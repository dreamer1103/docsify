## 分享几款适合初学者的C语言/C++开源项目

[CodeSheep](javascript:void(0);) *4月19日*

以下文章来源于程序员编程录 ，作者RioCoder

[![程序员编程录](http://wx.qlogo.cn/mmhead/Q3auHgzwzM6q6xx1Btmsia2v9MSGTlka0RDgDZvBhQzfib2DDpYBZmjA/0)**程序员编程录**来点务实的技术、优秀的项目、炫酷的软件](https://mp.weixin.qq.com/s/bRNiqhZZXaoRwPEt8GIpLg#)

![img](https://mmbiz.qpic.cn/mmbiz_png/vdXWcmzIVZHLHAMfKL4cOY9b60vaeckmcGqyiaFqcbZNbiaVychbicf4661p37d4a7VdiakJVYoYpVdvDa8GD21MJw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

------

# 说在前面

今天分享几款我收藏的适合初学者的C语言和C++领域的开源项目，有涉及**语言基础知识**的、有涉及**数据结构和算法题**的、有涉及**设计模式**的代码实现的，甚至还有涉及**效率工具和实践**的，希望能有帮助。

>  
>
> 后面会再分享一波 **Java领域** 的开源项目
>
> ”

------

# 项目一

**项目名称：** C

**项目简介：** 是的，你没有看错，这个项目的名字就是单个字母**C**。C是一个宝藏项目，可以说是学习数据结构和刷算法题的利器，因为里面包含了几乎各种基础算法、数据结构、以及LeetCode算法题的C语言实现。具体包括：

- 客户端/服务器问题
- 统计方法问题
- 进制转换问题
- 各种数据结构：数组、链表、字典、二叉树、堆、栈、队列、哈希、图等等
- 搜索/查找问题
- 排序问题
- LeetCode习题
- 其他杂项问题

注意，下图中只是截取了一部分数据结构和算法题的具体实现：

![img](https://mmbiz.qpic.cn/mmbiz_png/vdXWcmzIVZHLHAMfKL4cOY9b60vaeckmia72ibmoFd9AJE8WBOyOMkkMPofFzYFe7jvnECZtn9MCFia5gbGibwVhTQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**对于我们的作用：** 可以帮助我们更好的学习**数据结构**、以及**刷算法题**

**项目源码地址：** `https://github.com/TheAlgorithms/C`

------

# 项目二

**项目名称：** libhv

**项目简介：**`libhv`类似于`libevent`、`libev`和`libuv`，是一个跨平台的具有非阻塞I/O和计时器的异步事件驱动库，但`libhv`提供了更加简单易用的API接口并支持更加丰富的网络协议，基于它可以快速驱动HTTP服务端和客户端，从而提供高性能的`http`服务。

**主要技术点或特性：** 跨平台、事件循环、非阻塞I/O、支持IPv6、使用OpenSSL、支持多种网络协议

**对于我们的作用：** 可以帮助我们理解和实践**操作系统**的相关知识

**项目源码地址：**`https://github.com/ithewei/libhv`

------

# 项目三

**项目名称：** CPlusPlusThings

**项目简介：** CPlusPlusThings是一个适合初学者的从入门到进阶的仓库，里面包含了大量 C++语言的基础和进阶教程、源码剖析、工具推荐、实战练习等等，解决了初学者从入门到深入 C++的学习问题。

![img](https://mmbiz.qpic.cn/mmbiz_png/vdXWcmzIVZHLHAMfKL4cOY9b60vaeckmcA9oEl79MbbgsZETrDXBhb6dLQoJrlXasU1zS5IIF6wqjj4RiaKKVJQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**对于我们的作用：** 可以帮助我们系统地学习 **C++** 相关知识

**项目源码地址：** `https://github.com/Light-City/CPlusPlusThings`

------

# 项目四

**项目名称：** design-patterns-cpp

**项目简介：** 从项目名称就能够猜出来，这是一个C++语言版的设计模式实现，里面包含了常见设计模式的C++ 语言实现。

![img](https://mmbiz.qpic.cn/mmbiz_png/vdXWcmzIVZHLHAMfKL4cOY9b60vaeckmQuH40m7EcBljb8QQ8ibia4HwxQzM0iaqXZgH2EAEYfzjxdazIUd25wtrg/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**对于我们的作用：** 帮助我们理解和实践**设计模式**相关知识

**项目源码地址：** `https://github.com/JakubVojvoda/design-patterns-cpp`

------

# 项目五

**项目名称：**：tmux

**项目简介：** tmux一个开源免费的的终端复用软件。它的命令行界面非常炫酷易用，支持自由分割窗口，并且可以自由移动和调整，灵活且强大。一个非常强大的使用场景是：当远程连接到服务器使用时，只需要启动`tmux`，利用它就可以方便地进行后续操作，而无需打开多个ssh控制台窗口。

![img](https://mmbiz.qpic.cn/mmbiz_png/vdXWcmzIVZHLHAMfKL4cOY9b60vaeckmR9icSIF0vdclMOibQtvb8gsBno6UugLw67Nt8U1BDsficMvsd6HqW0w9g/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**对于我们的作用：** 既是一个高效的工具，研究源码也可以帮助我们学习和理解Linux环境实战编程。

**项目源码地址：** `https://github.com/tmux/tmux`

------

# 项目六

**项目名称：** netdata

**项目简介：** netdata是一款开源免费的炫酷Linux系统实时性能和运行状况的系统监控工具。netdata通过使用可交互的仪表盘形式，来提供灵活易用的系统监控。除了支持常见系统平台的安装之外，它还可以非常方便地安装于Docker容器和集群之中并提供监控服务。

![img](https://mmbiz.qpic.cn/mmbiz_png/vdXWcmzIVZHLHAMfKL4cOY9b60vaeckmjagicIHRLwq6NYiaV7aNzykAXjHAoG7rnzKibVUDniaeCAjDiaZaw8UWPkg/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**对于我们的作用：** 既是一个高效的工具，研究其源码也可以帮助我们学习和理解Linux环境实战编程。

**项目源码地址：** `https://github.com/netdata/netdata`

------

## **后记**

这次就先分享到这里吧，也感谢优秀的开源作者们付出的努力，后面有优秀的开源项目也会持续推荐的！

------

每天进步一点点，Peace！

2020.04.18 晚