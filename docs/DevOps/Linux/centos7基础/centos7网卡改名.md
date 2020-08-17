# centos7网卡改名
# 第一步查看服务器版本

```
[root@localhost ~]# cat /etc/redhat-release
CentOS Linux release 7.6.1810 (Core)
```

# 第二步查看当前网卡名称

我们可以看到当前网卡名称都是en0开头的，不方便我们集中管理

<!-- more -->

```
[root@localhost ~]# ip a
1: lo:  mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host
       valid_lft forever preferred_lft forever
2: eno1:  mtu 1500 qdisc mq state DOWN group default qlen 1000
    link/ether f4:1d:6b:86:8a:09 brd ff:ff:ff:ff:ff:ff
3: eno2:  mtu 1500 qdisc mq state DOWN group default qlen 1000
    link/ether f4:1d:6b:86:8a:0a brd ff:ff:ff:ff:ff:ff
4: eno3:  mtu 1500 qdisc mq state UP group default qlen 1000
    link/ether f4:1d:6b:86:8a:0b brd ff:ff:ff:ff:ff:ff
    inet 10.4.81.93/24 brd 10.4.81.255 scope global noprefixroute eno3
       valid_lft forever preferred_lft forever
    inet6 fe80::687f:25f8:b435:887b/64 scope link noprefixroute
       valid_lft forever preferred_lft forever
5: eno4:  mtu 1500 qdisc mq state DOWN group default qlen 1000
    link/ether f4:1d:6b:86:8a:0c brd ff:ff:ff:ff:ff:ff
```

# 第三步进入网卡配置文件

将所有的文件mv 更换名称

```
[root@localhost ~]# cd /etc/sysconfig/network-scripts/
[root@localhost network-scripts]# ls
ifcfg-eno1  ifcfg-lo     ifdown-ippp  ifdown-ppp     ifdown-TeamPort  ifup-bnep  ifup-isdn   ifup-ppp     ifup-TeamPort     network-functions
ifcfg-eno2  ifdown       ifdown-ipv6  ifdown-routes  ifdown-tunnel    ifup-eth   ifup-plip   ifup-routes  ifup-tunnel       network-functions-ipv6
ifcfg-eno3  ifdown-bnep  ifdown-isdn  ifdown-sit     ifup             ifup-ippp  ifup-plusb  ifup-sit     ifup-wireless
ifcfg-eno4  ifdown-eth   ifdown-post  ifdown-Team    ifup-aliases     ifup-ipv6  ifup-post   ifup-Team    init.ipv6-global
[root@localhost network-scripts]#
[root@localhost network-scripts]# mv ifcfg-eno1 ifcfg-eth0
[root@localhost network-scripts]# mv ifcfg-eno2 ifcfg-eth1
[root@localhost network-scripts]# mv ifcfg-eno3 ifcfg-eth2
[root@localhost network-scripts]# mv ifcfg-eno4 ifcfg-eth3
```

# 第四步修改网卡信息

> 需要修改的主要几点

> 1.NAME

> 2.DEVICE

> 3.BOOTPROTO [dhcp or static or none]none和static需要在输入ip地址

> 4.添加HWADDR 默认网卡没有mac地址，需要添加mac地址

![image_1d973tk0r17k91o41brp1ee11qjap.png-132.5kB](http://static.zybuluo.com/abcdocker/nm42x21fuesf06s8kee51jwf/image_1d973tk0r17k91o41brp1ee11qjap.png)

# 第五步修改内核参数

```
[root@localhost network-scripts]# vi /etc/sysconfig/grub
```

在倒数第二行quiet前面添加`net.ifnames=0 biosdevname=0`

![image_1d973vcu41cpv15241h7l3ju1p2k16.png-85.7kB](http://static.zybuluo.com/abcdocker/mtejm8isxl120hgxvqsca6v2/image_1d973vcu41cpv15241h7l3ju1p2k16.png)

我们还可以在装系统的时候配置

光标移动到`Install CentOS`上，按tab键 输入`net.ifnames=0 biosdevname=0` 回车

![image_1d97aftiu14lmkqh6pb11b6fad1j.png-21.2kB](http://static.zybuluo.com/abcdocker/397q3x5xs56yh134pjv1xsjx/image_1d97aftiu14lmkqh6pb11b6fad1j.png)

# 第六步生成启动菜单

```
[root@localhost network-scripts]#  grub2-mkconfig -o /boot/grub2/grub.cfg
Generating grub configuration file ...
Found linux image: /boot/vmlinuz-3.10.0-957.el7.x86_64
Found initrd image: /boot/initramfs-3.10.0-957.el7.x86_64.img
Found linux image: /boot/vmlinuz-0-rescue-f9f84382fb844c0a84e9ee9b2a2906b5
Found initrd image: /boot/initramfs-0-rescue-f9f84382fb844c0a84e9ee9b2a2906b5.img
done
```

# 第七步验证是否修改成功

```
[root@localhost ~]# reboot #重启生效
centos7默认不支持ifconfig,如果需要ifconfig请yum install net-t
```

修改完毕！

![8DBD4A93-15BF-4F34-B5D8-E9908CE368E0.png-568.3kB](http://static.zybuluo.com/abcdocker/e2smswto0wltzcwmzzbholsy/8DBD4A93-15BF-4F34-B5D8-E9908CE368E0.png)

![83092637-F388-4307-9682-2F0DFF534624.png-406.4kB](http://static.zybuluo.com/abcdocker/go8fefa9mwh3nv2rxt89yz5l/83092637-F388-4307-9682-2F0DFF534624.png)

![img](https://i4t.com/wp-content/uploads/2019/09/end.png)