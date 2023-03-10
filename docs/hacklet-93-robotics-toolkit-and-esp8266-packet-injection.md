# hacklet 93–机器人工具包和 ESP8266 数据包注入

> 原文：<https://hackaday.com/2016/01/30/hacklet-93-robotics-toolkit-and-esp8266-packet-injection/>

你永远不知道黑客会把你带到哪里。有时候，一个简单的项目会有自己的生命，并成为一个巨大的软件框架。其他时候，阅读博客可以变成一个周末项目。Hackaday.io 是上传每个项目的地方，无论是大项目、小项目还是介于两者之间的项目。在本周的 Hacklet 上，我们来看看两个项目——一个大项目，一个小项目。

[![wifi1](img/4d9779832a5f0bbac47b4db052696e0c.png)](https://hackaday.io/project/9333) 【兰德德鲁伊】最近在黑暗面度过了一个[周末，创造了一个 ESP8266 封包注入器。当[Rand]在 Hackaday 上读到](https://hackaday.io/project/9333)[[Kripthor 的] deauth 数据包注入攻击](http://hackaday.com/2016/01/14/inject-packets-with-an-esp8266/)时，这个项目就开始了。他最初创建了文章中提到的 WiFi 拒绝服务 throwie。该器件的基本物料清单(BOM)是一个 ESP8266 模块、一个 DC/DC 转换器、一个 9V 电池、连接器和几个电阻。这种方法效果很好，但一些设备(最明显的是兰德儿子的安卓手机)会很快断开和重新连接，因此攻击没有实际影响。

![double-wifi](img/6f5ace88415edd9e7bf8e1a96ab12cee.png)[Rand]通过添加第二个 ESP8266 模块修复了该问题。首先是听者。它监听 WiFi 接入点。一旦发现 AP，它就通过单向单线串行链路将该信息发送到第二干扰模块。干扰器模块全速泵出 deauth 数据包。他甚至设法创建了一个可执行文件，既能作为监听器又能作为干扰器。启动时，软件通过串行端口发送一系列 0xFF 字节。监听器的串行发射引脚直接连接到干扰机的串行接收线路。当干扰机接收到 0xFF 字节时，它会跳转到正确的功能。这足以将讨厌的安卓手机踢出网络。与原始文章一样，我们必须强调，您应该只在自己的设备上使用这样的模块进行测试。小心点，伙计们！

[![bowler](img/17d60fab476cfdf05979def192437c2f.png)](https://hackaday.io/project/6423) 【凯文·哈林顿】热爱机器人，但讨厌每次创造新机器都要重新发明轮子。他建立了[鲍尔斯工作室:一个机器人开发平台](https://hackaday.io/project/6423)来解决这个问题。鲍尔斯迪奥是 2015 年 Hackaday 奖的半决赛选手。BowlerStudio 是一个用于创建各种机器人的一应俱全的平台。[Kevin]已经将计算机辅助设计(CAD)、3D 建模、运动学、机器视觉和带有物理建模的模拟引擎集成到一个庞大的软件包中。为了证明该系统的多功能性，他在程序的 CAD 部分设计了一个六足机器人。然后机器人在模拟中自学行走。一旦设计被 3D 打印出来，真正的机器人就能从面包板上走下来。[凯文]将硬件和软件与他的另一个项目 [DyIO](https://hackaday.io/project/3185) 联系起来。

BowlerStudio 对于任何机器人黑客以及教育工作者来说都是一个巨大的福音。整个课程可以围绕这个系统创建。由于其 Java 根源，BowlerStudio 也是多平台的。[Kevin]已经为 Windows、Mac 和 Ubuntu 准备好了二进制文件。

BowlerStudio 的最新功能是 [JBullet](http://jbullet.advel.cz/) 。JBullet 是子弹物理库的 Java 端口。物理学意味着重力和表面摩擦等重要的现实世界效应现在可以添加到模拟中。用凯文自己的话说，“这个项目开始越来越像一个游戏引擎，旨在设计机器人和工程工具。”

这就是本周的 Hacklet。一如既往，下周见。同样的黑客时间，同样的黑客频道，带给你最好的 [Hackaday.io](https://hackaday.io/) ！

这就是本周的 Hacklet。一如既往，下周见。同样的黑客时间，同样的黑客频道，带给你最好的 [Hackaday.io](https://hackaday.io/) ！