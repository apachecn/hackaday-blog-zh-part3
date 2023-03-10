# 微动开关:越过临界点

> 原文：<https://hackaday.com/2017/04/17/microswitches-past-the-tipping-point/>

从 3D 打印机到喷气式客机，它们无处不在。它们是检测打印机卡纸的小开关，或者是感应电梯轿厢何时到达正确楼层的大型铠装开关。它们是*微型开关*，或者更确切地说是*微型快动开关*，它们如此常见，你可能永远不会好奇它们内部发生了什么。但是这些开关是如何被发明的背后的故事以及这些微小而有用的开关内部的物理原理都非常有趣。

### 小鸡开关

微动开关有着悠久的历史，至少从最初的注册商标“微动开关”成为通用术语开始就有了。早在 1932 年，威斯康辛州一家名为伯吉斯实验室的公司得到了一份订单，要建造 10，000 个电动小鸡孵卵器。该公司的老板查尔斯·伯吉斯向一家制造商订购了 10，000 台交换机，但沮丧地发现这些交换机并不符合标准。它们不会一直在同一个驱动点上切换，显然不会对他已经上钩的孵卵鱼起作用。Burgess 博士指派他的一名机械师开发一种更好的开关。Phillip McGall 最终想出了一个速动开关，具有小鸡孵卵器所需的可重复性，订单完成了。

几年后，麦克高尔为他的“快速开关”申请了专利 Burgess Labs 开始销售这种开关，并最终应用于 Rock-Ola 点唱机和不断增长的消费电子行业的其他机电产品。Burgess 最终卖掉了他的公司的电子部门，该部门后来变成了 Micro Switch Corporation，后来在 1950 年卖给了 Honeywell，至今仍是一个顶级品牌。

### 开始行动

[麦克高尔的快动开关背后的原理是一个*临界点机制*，其中他的开关中的公共触点是由预载弹簧制成的。](https://hackaday.com/wp-content/uploads/2017/03/microswitch.png)

弹簧力使触点保持稳定状态，顶住常闭触点。当通过致动器向公共触点施加少量压力时，预载弹簧在特征和可重复点变形，快速地将触点移动到另一个状态，抵抗常闭触点。重要的特征是通过致动器施加的力不直接移动常开和常闭之间的公共触点。移动公地的力量仅仅来自它的弹簧张力；致动器只提供使弹簧变形的力，直到弹簧弹出。

[![](img/ab184edf3e274fc49566afb75197e155.png)](https://hackaday.com/wp-content/uploads/2017/03/microswitch-e1490836921859.jpg)

A modern microswitch. By Benjamin D. Esham, [via Wikimedia Commons](https://commons.wikimedia.org/wiki/File%3AMicroswitch.jpg)

微动开关中的触点机制与普通触点相比有很多优点。该机制的可重复性很重要，快速的通断循环也是如此。一旦达到临界点，触点通常可以在几毫秒内转换状态。这减少了电弧放电的机会，并使触点处于模糊状态的时间最小化。

微动开关的另一个好处是操作力小。即使没有长杠杆臂支承在致动器上的机械优势，也仅需要少量的力来弹出弹簧并拨动开关。这种设计是灵活的，允许开关小到足以嵌入最小的步进电机，大到工业限位开关，设计用于在最恶劣的条件下生存，并持续数百万次循环。

现代的微动开关机制几乎与 McGall 的原始专利插图没有什么不同。当然，材料已经改变，并且已经有几种不同的设计用于预加载公共触点——例如碟形弹簧，或者叉形弹簧，其中中心“齿”锚定在与外部构件不同的平面中。但是这些简单装置的基本原理现在已经超过 75 年了，并且仍然在使用，这证明了良好的设计和坚实的工程技术。

 [https://www.youtube.com/embed/xaXNEySIqw4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xaXNEySIqw4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



横幅图片来源:[eRittenhouse.org](http://www.erittenhouse.org/articles/erittenhouse-vol-24-1-2012-2013/micro-and-reed-switches/)，作者艾伦·米尔斯。