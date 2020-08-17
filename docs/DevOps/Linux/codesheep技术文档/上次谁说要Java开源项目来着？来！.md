## 上次谁说要Java开源项目来着？来！

[CodeSheep](javascript:void(0);) *4月26日*

![img](https://mmbiz.qpic.cn/mmbiz_png/xq9PqibkVAzonjFbufTW1iaeKfa2iarTIAC4kmgouArVEO19V0B9Quj7trwggfxrdqSqXbZrUCceGGqMego8S6loA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

------

# 写在前面

前几天推荐C/C++开源项目（《[分享几款适合初学者的C语言/C++开源项目](http://mp.weixin.qq.com/s?__biz=MzU4ODI1MjA3NQ==&mid=2247485597&idx=1&sn=5e7f53ead683237f017dc352cab591d9&chksm=fddede59caa9574f4adc642b7aa7f77d476d2be3afa04649273f528a43d5c42808a6c32c3f50&scene=21#wechat_redirect)》）的时候，就有很多小伙伴留言说想要Java领域的开源项目。

实不相瞒，其实很久以前就推荐过一波优秀的Java开源项目了，内容在此：

[**《5款值得学习和练手的Java开源项目!》**](https://mp.weixin.qq.com/s?__biz=MzU4ODI1MjA3NQ==&mid=2247484967&idx=1&sn=a938733b3b2fbc18eac5dd7c29716c5b&scene=21#wechat_redirect)

当时推荐的几款主要包括后台管理项目、电商项目和微服务项目，今天**再来推荐**几个实用的Java开源项目，这算是第二波了。

------

# 项目一

**项目名称：** Java

**项目简介：** 这是一个基于Java的数据结构与算法的实现项目。里面包含了几乎常用所有**数据结构的实现**，以及诸多**算法题**和**LeetCode习题**的Java实现。主要包括：

- 加解密算法
- 进制转换
- 各种数据结构
- 分治
- 动态规划
- 数学类问题
- 搜索问题
- 排序问题
- LeetCode习题
- 其他杂项算法题等

![img](https://mmbiz.qpic.cn/mmbiz_png/xq9PqibkVAzonjFbufTW1iaeKfa2iarTIACyicQEV8LiaqqSelVs9Bj9r1q2QIyJezUtY8Ta2FwrQ369plzgsIWiaIJw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**对于我们的作用：** 基于Java语言的数据结构和算法题练手必备！

**项目源码地址：** https://github.com/TheAlgorithms/Java

------

# 项目二

**项目名称：** eladmin

**项目简介：** eladmin是一个基于 Spring Boot + Vue的前后端分离的后台管理系统，项目采用分模块开发方式， 权限控制采用 RBAC，支持数据字典与数据权限管理，支持一键生成前后端代码，支持动态路由，对于初学者还是比较友好的。

![img](https://mmbiz.qpic.cn/mmbiz_png/xq9PqibkVAzonjFbufTW1iaeKfa2iarTIACxMcwsibDmibxUicQTuC5AShvyGRtub6xB9TqFX3WJbWibFKxQFXsNiavD7A/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_png/xq9PqibkVAzonjFbufTW1iaeKfa2iarTIACoVWB53d87zvhYU0sgCjH3r7GcDPY9vhI29ZJtSibvlZRiaOVl88cboaw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**主要技术点或特性：**

- Spring Boot 2.x
- JPA
- Spring Security
- Redis
- Vue

**对于我们的作用：** 一套典型的后台管理系统，用的也是一套比较典型的Java后端开发技术，可以帮我们串联起很多后端开发的知识。

**项目源码地址：** https://github.com/elunez/eladmin

------

# 项目三

**项目名称：** jodd

**项目简介：**

Jodd **=** tools **+** ioc **+** mvc **+** db **+** aop **+** tx **+** json **+** html **< 1.7 Mb**

没错，Jodd是一个非常易用和好上手的**开源Java微框架**，里面包含了一系列平时经常会用到的一些**核心程序库**、**工具类/方法**、**实用程序/框架**等等。有了它，开发人员做起事来会变得非常简易和优雅，引入jodd就能帮我们快速实现某些功能。点赞！

![img](https://mmbiz.qpic.cn/mmbiz_png/xq9PqibkVAzonjFbufTW1iaeKfa2iarTIAC1YQEOoxWY9rq5ibgS1fcwEyGicaBPicl7BHbKTfbO0xWPQxYlCjdr22Zw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**主要技术点或特性：**

jodd主要包含：

- Jodd Libraries（程序库）：Json、Email、HTTP、Jerry ...
- Micro-frameworks（微框架）：Madvoc、Petite、Proxetta、DbOom ...
- Jodd Utilities（实用工具）：BeanUtil、Props、Decora、Cli、Ref ...

**对于我们的作用：** 一方面当我们想要用Java快速实现一些功能需求的时候，引入jodd就可以帮我们完成很多事情，很多工具和代码都开箱即用，简便高效；另外一方面研究其源码可以帮助我们打开技术视野。

**项目源码地址：** https://github.com/oblac/jodd

------

# 项目四

**项目名称：** SnowJena

**项目简介：**

SnowJena是一个基于令牌桶算法实现的分布式无锁**限流框架**，支持熔断降级，支持动态配置规则，支持可视化监控，开箱即用。可用于Java后端项目常见的本地限流和分布式限流的场景。

![img](https://mmbiz.qpic.cn/mmbiz_png/xq9PqibkVAzonjFbufTW1iaeKfa2iarTIACxibKgJ0lckh7SE6ZsufU4mGSD7KziaUpXv7pM9iaD3Sp5V68GAgjXsJOw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**主要技术点或特性：**

- 支持本地限流
- 支持分布式限流
- 支持黑白名单
- 支持可视化监控等。

另外项目用到了大量设计模式思想，包括单例模式、观察者模式、工厂模式、建造者模式等等。

**对于我们的作用：** 一是帮助我们学习和实践**限流**这一常见的技术方案和实现原理，二是帮助我们学习和理解常见的**设计模式**。

**项目源码地址：** https://github.com/ystcode/SnowJena

------

# 项目五

**项目名称：** seata

**项目简介：** Seata 是一款阿里巴巴开源的**分布式事务**解决方案，致力于在微服务架构下提供高性能和简单易用的分布式事务服务。

![img](https://mmbiz.qpic.cn/mmbiz_png/xq9PqibkVAzonjFbufTW1iaeKfa2iarTIAC4ibCvzjO8yEvBfJgMWNxBVg6T5PNlxTeZVk5FMicjV2XicGqcCwCB0IKg/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

在 Seata 开源之前，Seata 对应的内部版本在阿里内部一直扮演着分布式一致性中间件的角色，而且应用于历年的双11场景。2019年1月，为了打造更加完善的技术生态和普惠技术成果，Seata 正式宣布对外开源了。

![img](https://mmbiz.qpic.cn/mmbiz_png/xq9PqibkVAzonjFbufTW1iaeKfa2iarTIAC4UW7Ricg15kdM8dnl2ZYUpY3gAiaMyVHcDPYGYh6Y9fecXAFialJFiaQibw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**主要技术点或特性：**

- 支持常见主流的微服务框架
- 支持AT模式
- 支持TCC模式
- 支持SAGA模式
- 高可用和强大的横向扩展能力

**对于我们的作用：** 分布式事务问题几乎是当下后端开发和架构领域**最棘手**和**最有含金量**的问题之一，多学点总是好的。

**项目源码地址：** https://github.com/seata/seata

------

# 后记

感谢这些优秀的开源作者和优秀的开源项目，我们站在具人的肩膀上，看得更好，走得也更远！

------

每天进步一点点，Peace！

2020.04.25 深夜