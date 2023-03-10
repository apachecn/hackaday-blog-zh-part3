# 这是会议徽章获得自己的徽章的一年

> 原文：<https://hackaday.com/2018/06/21/this-is-the-year-conference-badges-get-their-own-badges/>

在过去的几年里，印刷电路板的艺术和艺术性已经从名片转移到所有一次性电子产品中最受欢迎的。当然，我说的是贝格利弗。这是一个在全球各种技术和安全会议上创建和分发独立电子会议徽章的社区。

到目前为止，badgelife 一直是一个由 badgemakers 和 distributors 组成的松散联盟，每年都用更令人印象深刻的电路板、技术和更闪亮的珠宝超越自己。该领域发展如此之快，以至于无法与过去几年所做的事情相提并论；十年前，一个简单的 PCB 和闪烁的 LED 就足够了，现在我们已经从工厂直接定制了微控制器，新奇的新芯片，以及你所见过的最伟大的艺术。

现在我们已经达到了一个门槛。badgelife 社区已经变得如此之大，徽章也有了自己的徽章。今年是徽章附加年。我们都在为我们的徽章制作小饰品，这一次，它们将一起工作。我们离一个由徽章制成的可爱机器人只有一年了。

## 徽章附件的前期历史

尽管今年会议徽章的附件将席卷赌场，但这绝不是徽章时代的开始。

[![](img/48e29ecb3442c12f2d11f7b6afb090ea.png)](https://hackaday.com/wp-content/uploads/2018/06/queercon2016.jpg) 附加产品标准化规格的起源始于[2016 queer CON 徽章](https://hackaday.com/2016/08/10/what-we-learned-from-the-2016-queercon-badge/)，在 DEF CON 24 上分发。这个徽章，要么是乌贼，要么是墨鱼，有两个四针的“帽子”头。戴帽子的原因很简单 2016 Queercon 徽章的主要特点之一是使用透明阻焊膜，使徽章具有可爱的未氧化铜饰面。然而，Queercon 组织者的“优步”徽章和其他人的普通“人类”徽章之间必须有所区别。传统上，这是用不同颜色的阻焊膜来完成的。没有这个选择，奎尔孔转向字面上的发光帽子。优步帽是一顶亮色礼帽,“训导员”帽是一顶装着 555 手枪的红色警察帽，普通的“人”帽是一顶顶部有螺旋桨的无檐帽。

在 DEF CON 前几周，Queercon 帽子的规格被泄露，这意味着一些人能够制作自己的配件。发光的独角兽角可能是最受欢迎的，甚至有几个 emo 发型 PCB 出现在 Queercon 徽章上:

[![](img/16593455b53ea1bb04c06b96950dd49e.png)](https://hackaday.com/wp-content/uploads/2018/06/queerconuserhats.jpg)

2016 Queercon 徽章的附加组件非常成功，并通过官方徽章支持的独立附加组件展示了社区的创造力。附加徽章的想法被其他小组采纳，[2017 saint con 徽章](http://saintcon.gitlab.io/Badge2017/)装载了独立附加的扩展标题。

[![](img/912b6766c01a3880ace1cdbee95ee45c.png)](https://hackaday.com/wp-content/uploads/2018/06/brainslug.png)

2017’s AND!XOR badge featured a brainslug add-on

2017 Saintcon 徽章包含四个用于附加设备的空间，在 0.8 英寸见方的面积上排列成两个 8 针接头。创造一个实用而有趣的附加功能的一切都在那里:附加徽章有 SPI、I2C 以及 5 伏*和* 3.3 伏的连接。

结果是惊人的:有很多非官方的迷你徽章被焊接到 Saintcon 徽章上，包括来自[compukidmike]的令人印象深刻的 8×8 LED 矩阵。在 2017 年的剩余时间里，附加内容被硬塞到其他徽章中。去年的[班德徽章来自和！XOR](https://hackaday.com/2017/07/12/hands-on-new-andxor-unofficial-def-con-badge/) 有一个附加的标题，还有一个为机组成员准备的奇妙的[脑残附加](https://github.com/ANDnXOR/ANDnXOR_DC25_Badge/tree/master/Brain%20Slug)。

到 2018 年初，很明显附加产品将会成为一种东西。2016 Queercon 附加组件的简单性非常出色，证明了为附加组件添加标题并不是很难，也不应该花费任何成本。每个微控制器都有 I2C，如果你正在设计一个徽章，你会在某个地方有一个电源轨。

## 附加组件标准的开始

[![](img/ea8d1697f55317b1bc73abf3b8baebcd.png)](https://hackaday.com/wp-content/uploads/2018/06/shitty-add-on-standard.png)

The standard for Shitty Add-ons. Note the Comic Sans

今年年初，很明显必须有一个徽章附加产品的标准。2 月份，badgelife 社区正忙于他们徽章的初始布局，每个人都需要某种标准的电源、接地和微控制器连接引脚。

这导致了低劣的附加标准的产生。简单地说，这是将迷你徽章添加到其他徽章的最简单方法:间距为 0.1 英寸的 2×2 标题。没有电流限制，没有极性保护。如果你插错了插件，它会杀死主徽章。事实上，这就是一些附加产品的全部意义。这些附件的机械稳定性很差，如果你使用表面贴装引脚，它们会脱落。

简而言之，这个插件规范是由一个微软画师的白痴在十分钟内设计出来的。

然而，低劣的附加规范有一个很大的优点:实现起来非常简单。几乎每个为今年 badgelife 盛会制作的徽章都将有一个 3.3 伏的轨道。每个微控制器在某处都有一条 I2C 总线。0.1”引脚接头也很便宜。它有问题，但是低劣的附加规范是支持多个附加徽章的最简单的方法。

## 今年的“劣质附加产品”

我们距离 badgelife 的主要活动 DEF CON 还有几周时间，徽章创作者的艺术和艺术性已经令人难以置信。将会有几十个不同的低劣附加组件，每个都展示了社区的非凡工艺:

 [![@d4rkwyng's Mr. Meeseeks Shitty Add-On](img/6fb357dd8d52620e22581c6f1f1e8f48.png "LookAtMe")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/06/lookatme.png?ssl=1) @d4rkwyng’s Mr. Meeseeks Shitty Add-On [![@sqearlsalazar's Baby Bender add-on](img/a89e7fe7afb5186b348d2ef48a346553.png "DeFFAzeU0AISMJb")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/06/deffazeu0aismjb.jpg?ssl=1) @sqearlsalazar’s Baby Bender add-on [![@mrtwinkletwink's pika and terrifying Krusty add-on](img/1d2f73b4d2c5aab60da4edf8054e60d5.png "DfIPMWIWkAA7YPf")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/06/dfipmwiwkaa7ypf.jpg?ssl=1) @mrtwinkletwink’s pika and terrifying Krusty add-on [![@Borgel's light-up taco add-on, along with the add-on version of Hackaday's official DC25 badge](img/cd70700c5d3d266dd1c4a783752483d3.png "DdmzLN7UQAA_0tV")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/06/ddmzln7uqaa_0tv.jpg?ssl=1) @Borgel’s light-up taco add-on, along with the add-on version of Hackaday’s official DC25 badge [![@sqearlsalazar's Fry add-on](img/a765142ffc858d03c95153781ec6b1e3.png "DfC_h6IVQAALzTa")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/06/dfc_h6ivqaalzta.jpg?ssl=1) @sqearlsalazar’s Fry add-on [![@borgel's taco, with this year's dragonfly badge](img/5b87c71979273a4891c1aaefb52960a3.png "Taco")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/06/taco.jpg?ssl=1) @borgel’s taco, with this year’s dragonfly badge

这些只是 badgelife 社区正在制作的一小部分附加产品。

对于电子徽章来说，这是一个辉煌的一年。我们甚至不知道官方的 DEF CON 徽章会是什么，但是独立的 badgelife 社区今年正在设法做一些引人注目的事情。如果你把插件算作独立的徽章，那么今年的 DEF CON 上的独立徽章完全有可能会比参会人数更多。让那件事过去一会儿。DEF CON 无法为每个人创建足够多的电子徽章，这里我们有一个徽章创建者社区，他们不仅为每个人创建了足够多的徽章，还创建了一个每个人都可以尝试的平台。

## 这对你意味着什么

Badgelife 是一个硬件演示。badgelife 社区正在用玻璃纤维和阻焊膜来制作电子产品，而不是用 Commodore 或 Amiga 来组装。这是一个设计和工程的开放季节，这一切都发生在今年夏天世界各地的各种技术和安全会议上。

低劣的附加标准是 Badgelife 最简单的入门方式。今年发行的几乎每一个主要徽章都将配有合适的头部，电源会为您提供，您所要做的就是拿出一个伟大的设计，并找出一种让一些 led 闪烁的方法。

今年是徽章获得徽章的一年，这是开始设计自己的 PCB 的最佳时机。这是硬件演示，现在对每个人开放。