# JST 不是一个连接器

> 原文：<https://hackaday.com/2017/12/27/jst-is-not-a-connector/>

当阅读一些很酷的项目和产品时，经常会看到标有“JST 连接器”的接线插头。这看起来很好，直到我们开始动手，开始一起动手。不可避免地，我们会发现一个部分的 JST 连接器不适合另一个部分的 JST 连接器。这是我们了解“JST”不是连接器规范的时刻。是[日本无焊端子制造株式会社](http://www.jst-mfg.com/)的简称。这家公司的历史[可以追溯到 1957 年](http://www.jst-mfg.com/profile/index.php?lang=en_US#corporateHistory)，他们的网站(1999 年改版)列出了数百种不同类型的。

在谈论项目时，我们可以简化为“JST 连接器”。但是当涉及到实际的硬件规格时，这还不够好。*哪个* JST 连接器？

[![](img/c6519058195a6bf16dfa673afb2dea15.png)](https://hackaday.com/wp-content/uploads/2018/12/lipoly-jst-rcy-and-xh.jpg)

Battery pack with JST RCY for discharging and JST XH for balance charging.

现实是:我们生活在一个充满模糊连接器规范的世界。我们有时也选择忽略“内部没有用户可维修的部件”,愉快地探索我们根本没有规格的设备内部。作为黑客，我们需要一些破译神秘连接器的技巧。我们将从快速调查 JST 中最流行的类型开始。

一个简单的两针线对线连接器可能是 [RCY](http://www.jst-mfg.com/product/detail_e.php?series=521) 系列。当连接器将两根或多根导线连接到电路板时，它可能是以下系列之一。缩小候选人范围的一个快速方法是看他们的间距:引脚之间的距离。那么识别就变成了将物理特征与数据表进行比较的问题。

[![](img/e946ad693ad06f2d4dfbb0b69c8cb0ce.png)](https://hackaday.com/wp-content/uploads/2018/12/3d-printer-jst-xh.jpg)

3D printer control board with JST XH connection to the stepper motors

我们从 JST XH 系列开始。它的间距为 2.5 毫米，与原型试验板上常见的 0.1 英寸间距完全相同。XH 系列之后，通过[PH](http://www.jst-mfg.com/product/detail_e.php?series=199)(2.0mm)[ZH](http://www.jst-mfg.com/product/detail_e.php?series=287)(1.5mm)[GH](http://www.jst-mfg.com/product/detail_e.php?series=105)(1.25mm)[SH](http://www.jst-mfg.com/product/detail_e.php?series=231)(1.0mm)，引脚间距变窄，线材变细，连接器更脆弱。SH 系列是如此之小，以至于 JST 指定了可选的突出物来给我们一些东西。

如果一个神秘的连接器与流行的 JST 连接器的数据表不匹配，那么不幸的是，搜索变得更加困难。当面对这个深入挖掘的任务时，请记住它可能根本不是 JST 连接器。过剩库存经常被贴错标签，一些连接器看起来太像了。 [Molex PicoBlade](http://www.molex.com/product/picoblade.html) 是一种 1.25 毫米间距的连接器，经常与 JST GH 混淆。

[![](img/e49647798ff8c4136d68c069b86afddc.png)](https://hackaday.com/wp-content/uploads/2018/12/not-jst-sh.jpg)

This mystery “JST connector” has the 1 mm pitch of the JST SH, but the datasheet says it is too large to be one.

随着我们获得连接器方面的经验，我们将根据上下文做出更好的猜测。后院友好的业余爱好飞机生态系统(飞机、直升机和多旋翼)使用了许多由 JST 设计的连接器，Molex 是一个较小的参与者。在 PC 组件领域，情况正好相反，Molex 设计了该生态系统中的大多数连接器。

在选择连接器时，这些知识会派上用场。通常，一次性项目中使用的连接器是由其他人构建的组件上的连接器决定的，但有时选择是由我们做出的。如果我们了解项目的背景并选择符合现有惯例的东西会更好。

当你做出选择时，在你的项目文档中要具体。没有必要让别人(可能是你未来的自己)去猜测你用的是哪种连接器。

这对于组件厂商来说就更重要了。尽管互联网规范普遍较差，但这并不是懒惰的借口。客户需要知道与您的产品接口的具体连接器。

有助于防止未来的麻烦:具体到你的连接器！