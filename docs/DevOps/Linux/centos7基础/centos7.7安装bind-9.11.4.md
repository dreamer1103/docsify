## Centos7.7安装bind-9.11.4

[TOC]

<img src="http://img.ymw.cn/52017121314000f821e4f.jpg" alt="avatar" style="zoom:150%;" />/

<!-- more -->

##  一.基础环境准备

1.1设置主机名

~~~bash
hostnamectl set-hostname jmds1-11.host.com   #jmds1-11生产方式常用地点命名主机方式
~~~

1.2关闭防护墙和selinux

~~~bash
systemctl stop firewalld
systemctl disable firewalld
setenforce 0
sed –i ‘s/SELINUX=enforcing/SELINUX=disabled/g’ /etc/selinux/config
~~~

1.3设置网卡

~~~bash
cat /etc/sysconfig/network-scripts/ifcfg-eth0 
TYPE=Ethernet
BOOTPROTO=none
NAME=eth0
DEVICE=eth0
ONBOOT=yes
IPADDR=172.16.1.11
NETMASK=255.255.255.0
GATEWAY=172.16.1.254
DNS1=172.16.1.254
~~~

1.4设置yum源和epel源

~~~bash
wget -O /etc/yum.repos.d/CentOS-Base.repo  http://mirrors.aliyun.com/repo/Centos-7.repo
wget -O /etc/yum.repos.d/epel.repo  http://mirrors.aliyun.com/repo/epel-7.repo
yum clean all
yum makecache
~~~

1.5安装常用工具

~~~bash
yum install wget net-tools telnet tree nmap sysstat lrzsz dos2unix bind-utils -y
~~~

## 二.安装bind服务

2.1安装bind-9.11.4服务

~~~bash
yum install bind -y
~~~

2.2配置bind 9

~~~bash
vi /etc/named.conf                      #配置主文件named.conf
listen-on port 53 { 172.16.1.11; }; 
allow-query     { any; };
forwarders      { 172.16.1.254; };      #下一级DNS
recursion yes;
dnssec-enable no;
dnssec-validation no
##############
named-checkconf            #检查named.conf文件语法
~~~

~~~bash
vi /etc/named.rfc1912.zones      #配置域文件也可以在主文件里配置一样的
zone "host.com" IN {             #主机域
        type  master;
        file  "host.com.zone";
        allow-update { 10.4.7.11; };
};

zone "md.com" IN {               #业务域MD市场部
        type  master;
        file  "od.com.zone";
        allow-update { 10.4.7.11; };
};
~~~

~~~bash
cp -p /var/named/named.localhost /var/named/host.com.zone     #模板拷贝两个域加-p保持属性
cp -p /var/named/named.localhost /var/named/md.com.zone
vim /var/named/host.com.zone
$TTL 1D
@   IN SOA  @ rname.invalid. (
                    0   ; serial
                    1D  ; refresh
                    1H  ; retry
                    1W  ; expire
                    3H )    ; minimum
    NS  @
    A   172.16.1.11
    AAAA    ::1
jmds1-11 A 172.16.1.11
jmds1-12 A 172.16.1.12
jmds1-21 A 172.16.1.21
jmds1-22 A 172.16.1.22
jmds1-200 A 172.16.1.200

vim /var/named/md.com.zone
$TTL 1D
@   IN SOA  @ rname.invalid. (
                    0   ; serial
                    1D  ; refresh
                    1H  ; retry
                    1W  ; expire
                    3H )    ; minimum
    NS  @
    A   172.16.1.11
    AAAA    ::1

named-checkconf                                          #检查主配置文件语法
named-checkzone zone /var/named/host.com.zone            #检查域配置文件语法
zone zone/IN: loaded serial 0
OK
named-checkzone zone /var/named/md.com.zone
zone zone/IN: loaded serial 0
OK
~~~

2.3检查配置并启动bind 9

~~~bash
systemctl start named
netstat -lntup|grep named
dig -t A hdss7-11.host.com @10.4.7.11 +short
ping jmds1-11
PING jmds1-11.host.com (172.16.1.11) 56(84) bytes of data.
64 bytes from jmds1-11.host.com (172.16.1.11): icmp_seq=1 ttl=64 time=0.006 ms

###如果systemctl start named启动不了报错，直接用 named -u named 可以启动，如果要习惯 systemctl restart named.service启动的话，注释掉下面文件一行
vim /usr/lib/systemd/system/named.service
#ExecStartPre
#注释ExecStartPre 不检查 zone
~~~

2.4配置DNS客户端

~~~bash
vim /etc/sysconfig/network-scripts/ifcfg-eth0
DNS1=172.16.1.11
##########
vim /etc/resolv.conf
search host.com
nameserver 172.16.1.11
##########
systemctl restart network
~~~

完成配置！！！