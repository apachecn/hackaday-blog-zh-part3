# Hackaday 奖参赛作品:电动变桨距道具

> 原文：<https://hackaday.com/2017/04/03/hackaday-prize-entry-electric-variable-pitch-props/>

除了最小的有人驾驶飞机之外，大多数由螺旋桨驱动的飞机都有可变螺距螺旋桨。原因很简单，就是效率。内燃机在特定的转速下效率最高，飞行员可以简单地改变螺旋桨的螺距，而不是给发动机更多的气体来加速。对于气体动力发动机，变距螺旋桨的机械和设计已经很好理解，几十年来并没有真正改变。给由电动机驱动的东西增加可变螺距螺旋桨完全是另一回事。这就是[彼得·麦克劳德]为参加黑客日奖而建造的东西，它将成为可以想象的最酷的项目。

这个项目是为以前的 Hackaday 奖参赛作品设计的，也是 2014 年唯一一个没有杀死任何人的 Hackaday 奖参赛作品。 [Goliath 是一架由割草机发动机](https://hackaday.io/project/1230-goliath-a-gas-powered-quadcopter)驱动的四轴飞行器，虽然它将悬停在【彼得】的测试台上，但他没有获得他预期的升力，控制系统需要工作。有两种可能的解决方案来解决控制脱瓣器的问题:[一种灵活的网格鳍](https://hackaday.io/project/1230/log/55717-control-hardware-starting-to-take-shape)或可变螺距转子的应用。[Peter]不知道这两种解决方案是否可行，所以他同时在研究这两种解决方案。

[Peter]的可变螺距旋翼系统基本上是一个电子螺旋桨支架，直接连接到他的气动四轴飞行器的驱动轴上。为了给电子设备供电，[彼得]正在将永磁体安装到四轴飞行器的框架上，从转子轮毂的线圈中获取电力，并将其整流到 DC，以驱动伺服系统和电子设备。道具的控制将通过 ESP32 微控制器无线完成。

可变螺距道具是从水坑跳伞运动员到杂技遥控直升机的标准配置。在四轴飞行器的世界里，变桨距道具充其量只是一个注脚。麻省理工学院 ACL 实验室已经做了类似的事情，但也许与[彼得]正在做的事情最好的比较是令人难以置信的黄貂鱼 500 quad。 [Flite Test 对这个 quad](https://www.youtube.com/watch?v=TnGhEInTXYc) (YouTube)做了一个很好的概述，它非常类似于 Goliath 的未来版本。一个大电机(在黄貂鱼的情况下，是一个无刷电机)通过一条皮带为所有的道具提供动力，道具的俯仰由四个伺服系统控制。这些可变螺距四轴飞行器的机动性令人难以置信，但由于 Goliath 如此之大，质量如此之大，很怀疑[Peter]会用他的四轴飞行器做翻转和翻滚。

你可以在下面看看[彼得]的视频。

 [https://www.youtube.com/embed/BXtvvZkaH_8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/BXtvvZkaH_8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)