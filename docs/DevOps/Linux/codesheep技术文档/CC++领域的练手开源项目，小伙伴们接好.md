## C/C++领域的练手开源项目，小伙伴们接好

[CodeSheep](javascript:void(0);) *1月8日*

小伙伴们大家好，今天又是元气满满的一天！

话说之前其实已经推荐过Java和Python这两个领域的一些值得初学者学习和练手的开源项目：

- [5个值得学习和练手的Java企业级开源项目](http://mp.weixin.qq.com/s?__biz=MzU4ODI1MjA3NQ==&mid=2247484967&idx=1&sn=a938733b3b2fbc18eac5dd7c29716c5b&chksm=fdded0e3caa959f54aa411f86921fe1f4ca1e37e9c54391d772a9794f3b28b089adf118193cd&scene=21#wechat_redirect)
- [推荐几个炫酷的Python开源项目](http://mp.weixin.qq.com/s?__biz=MzU4ODI1MjA3NQ==&mid=2247484209&idx=1&sn=9db7e839ca1f271cc0553297ca6f0fc6&chksm=fdded5f5caa95ce36ef6f7bc642c50c0c9396b64476f4b217e5de0f4f743295a64fa96e69a6e&scene=21#wechat_redirect)

今天应大家要求，再来继续推荐几个我收藏的，关于C语言和C++领域的适合初学者学习和练手的开源项目，供大家参考。

学完编程语言感觉还只是玩具，其实也挺常见，主要是因为没有足够的实战和练手，花点时间好好研读这些开源项目大有裨益。大家可以认真**吸收**这些项目并真正**转化为**自己的技能点，这样以后不管是**复试**、**写简历**亦或是**求职找工作**，也能更加从容一点！

![img](https://mmbiz.qpic.cn/mmbiz_png/xq9PqibkVAzotWUYMzMur1y8X3kPrJxyRwUyjkKBANiaPPRwrCXT286fEUw7okmV4kx9MFibpQg2bHjVXoLzbicpFw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

> 必须要说的是，不像Python，Java等开源项目一般都具备美观的可视化界面、网页、甚至手机App；而C语言和C++写的项目一般非常朴素，大多运行于命令行那个简单的黑乎乎界面，甚至完全运行于后台。

------

 **Tinyhttpd** 

**项目名称：** Tinyhttpd

**项目简介：**Tinyhttpd 是J. David Blackstone在1999年写的一个不到 500 行的超轻量型 Http Server，用来学习非常不错，可以帮助我们真正理解服务器程序的本质。建议源码阅读顺序为：`main->startup->accept_request->execute_cgi`, 通晓主要工作流程后再仔细把每个函数的源码看一看。这500行代码吃透了，C语言的功底就会大幅提升。

![img](https://mmbiz.qpic.cn/mmbiz_png/xq9PqibkVAzotWUYMzMur1y8X3kPrJxyRhtIm9wok3zC6QpNWU9HlC0GxemS6yxM0ia90vNHu6yiaGdrEZmic6V3mw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

【注：图片来源于：www.cnblogs.com/nengm1988/p/7816618.html】

**项目源码：**https://github.com/EZLippi/Tinyhttpd

------

 **tmux** 

**项目名称：** tmux

**项目简介：** tmux一个炫酷的终端复用软件，它提供了一个非常易于使用的命令行界面，可横向和纵向分割窗口，窗格可以自由移动和调整大小，而且还可以通过交互式菜单来选择窗口、会话及客户端。类似的终端复用器还有 GNU Screen。Tmux 与它功能相似，但是更易用，也更强大。大名鼎鼎的阮一峰老师还写过tmux的使用教程，大家也可以看一看

![img](https://mmbiz.qpic.cn/mmbiz_png/xq9PqibkVAzotWUYMzMur1y8X3kPrJxyRwM4ujOia7IIzpK1paChO0Npwhmel5wDAAicBptNvjRh1r77w4G1XZ52w/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**项目源码：**https://github.com/tmux/tmux

------

 **musikcube** 

**项目名称：** musikcube

**项目简介：** musikcube是一个使用C ++编写的跨平台，运行于终端上的音乐播放器。musikcube可以在Windows，macos和linux上轻松编译和运行。它也可以在带有raspbian的树莓派上很好地运行，并且可以设置为流音频服务器。炫酷得一腿。

![img](https://mmbiz.qpic.cn/mmbiz_png/xq9PqibkVAzotWUYMzMur1y8X3kPrJxyRAN7tN0Wbb0EL5XG6Ric63ABdCIicibGl9cvZ47o5fEAP5Mpb3cemSzd3w/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**项目源码：**https://github.com/clangen/musikcube

------

 **MyTinySTL** 

**项目名称：** MyTinySTL

**项目简介：** 很多人表示学完C++不知道用来干什么，我觉得学完C++的第一个练手的好机会那就是自己试着实现一个小型的STL库。MyTinySTL的作者它就用 C++11 重新复写了一个小型 STL（容器库＋算法库）。代码结构清晰规范、包含中文文档与注释，并且自带一个简单的测试框架，非常适合新手学习与参考！

![img](https://mmbiz.qpic.cn/mmbiz_png/xq9PqibkVAzotWUYMzMur1y8X3kPrJxyRl0ogZiacBZxkbSDMicAiaab5V4fArePQatLj3WJVRFbzFpH8LrKsny6XQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**项目源码：**https://github.com/Alinshans/MyTinySTL

------

 **oatpp** 

**项目名称：** oatpp

**项目简介：** 我们知道Java领域的Web框架非常繁荣，最知名的当属Spring全家桶，而C语言和C++阵营则几乎没有。那oatpp则是一个轻量、跨平台、高性能、完全零依赖，用纯 C++ 实现的 Web 框架，实在是难得，小伙伴们可以学习学习。

![img](https://mmbiz.qpic.cn/mmbiz_png/xq9PqibkVAzotWUYMzMur1y8X3kPrJxyRn9WbSyzYj41cKbdfLwibRyJnFj6BuVlkgtTz60YNiaib8TgcAUbHVibAbA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**项目源码：**https://github.com/oatpp/oatpp

------

 **muduo** 

**项目名称：** muduo

**项目简介：** muduo是一个基于Boost库实现的现代C++高并发网络库，由陈硕大神编写。它一个高质量的事件驱动型的网络库，其核心代码不超过4500行，使用 `non-blocking IO(IO multiplexing)` + `one loop per thread`模型，适合开发 Linux 下的多线程服务端应用程序，通过阅读源码还可学习到 C++ 语言、Linux 网络编程等后端知识。

![img](https://mmbiz.qpic.cn/mmbiz_png/xq9PqibkVAzotWUYMzMur1y8X3kPrJxyRJAyhLZ3EPg76qefSgUnG2aXSZdn5712ZLBBODL095zSQxtQtkP6MjA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**项目源码：**https://github.com/chenshuo/muduo

------

 **CppNet** 

**项目名称：** CppNet

**项目简介：** CppNet一个封装在 TCP 协议上的 Proactor 模式 multi-thread 网络库。包含 OS 接口调用、回调处理、定时器、缓存管理等，这里有从操作系统到应用层的所有网络细节，便于初学者学习和实践。

- 简单：只导出了最少量的接口，其声明都类似系统 socket API。对客户端而言，只新增了一个 buffer 类型
- 快速：采用性能最优的 epoll 和 IOCP 做事件驱动。每个连接都独享一个内存池，从内存池中申请的内存都由智能指针管理
- 清晰：结构上分为事件驱动，会话管理，接口三层，通过回调向上通知。模块之间职责分工明确，最大的类不超过 500 行代码

![img](https://mmbiz.qpic.cn/mmbiz_png/xq9PqibkVAzotWUYMzMur1y8X3kPrJxyRHlcW4ZBVic3u8CBpAOp0xgtdNe1d7ibUvt2j8g2C7sFiaFRpyJe5s8tng/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**项目源码：**https://github.com/caozhiyi/CppNet

------

每天进步一点点！Peace！

2020.01.07晚