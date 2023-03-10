# 哈雷机车的数字转速表

> 原文：<https://hackaday.com/2017/05/08/a-digital-tacho-for-a-harley/>

如果你是一个摩托车爱好者，你可能会被归入不同的车手群体中。也许你是一个总是想让膝盖着地的运动自行车爱好者，一个不努力就让膝盖着地的超级摩托车手，一个在真正骑行之间觉得柏油路很烦人的拖车骑手，或者一个花更多时间在车间而不是骑行的经典自行车爱好者。

泽维尔·莫拉莱斯(Xavier Morales)却不是这样，因为他骑着哈雷戴维森跑车在家乡加泰罗尼亚的公路上巡游。如果你只在流行文化中熟悉哈雷，或者你是一个嘲笑它们不合时宜的操控和刹车的运动自行车骑手，那么从技术角度看一下现代哈雷是值得的。尽管造型和品牌精神唤起了另一个时代，商标大型 V 型双引擎在外行人看来与几十年前一样，但今天的哈雷是一台非常现代的机器，比嘲笑运动自行车手的人认为的更有能力。

然而，有一个领域是[Xavier]的哈雷非常缺乏的。它唯一的仪器是速度计，没有转速表。你可能会认为，与转速较低的哈雷发动机相比，这对于转速较高的日本运动自行车来说不算什么问题，但这足以让他恼火，因为他自己造了一个转速表。他对这个项目的报道既冗长又引人入胜，非常值得一读。

Sportster 的数据总线遵循已建立但已过时的标准，SAE J1850 VPW。由于这种总线的驱动芯片已经停产，他不得不使用一个晶体管和几个电阻来创建自己的芯片。一旦他有了数据，他就把它输入 PIC 18F2553，PIC 18f 2553 又运行一个显示驱动芯片来控制一对 7 段 led。还有一组发光二极管指示齿轮变化。整个系统安装在一个 3D 打印的外壳中，与原来的速度计放在一起，在另一个表盘的玻璃后面。因此，这款自行车看起来似乎一直是双时钟设计，具有专业的外观。

如果你想看实际操作，他已经发布了几个视频，我们也在休息时间下面放了一个。美丽的加泰罗尼亚风光和蜿蜒的山脉看起来非常诱人。

 [https://www.youtube.com/embed/WTcDo77_0HA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/WTcDo77_0HA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



如果自行车是你的东西，那么我们多年来已经推出了不少。然而令人难忘的是[这个燃气轮机怪物](http://hackaday.com/2014/07/25/you-might-be-cool-but-youre-not-gas-turbine-motorcycle-cool/)和[这个灾难性的首次框架建造尝试](http://hackaday.com/2016/07/12/fail-of-the-week-how-not-to-build-your-own-motorcycle/)。