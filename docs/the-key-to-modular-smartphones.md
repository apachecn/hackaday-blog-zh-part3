# 模块化智能手机的关键

> 原文：<https://hackaday.com/2015/10/30/the-key-to-modular-smartphones/>

手机初创公司 [Fairphone](https://www.fairphone.com/) 正在[接受他们模块化智能手机的预购](http://arstechnica.co.uk/gadgets/2015/10/fairphone-2-hands-on-modular-phones-are-finally-here/)，预计将于今年 12 月开始发货。虽然我更熟悉谷歌的 project Ara，但这是第一个推向市场的模块化概念。不过，这确实让我想到了几个问题:这实际上是一款模块化智能手机吗？模块化概念会被广泛采用吗？

### 理论上伟大，实践上可疑

![Camera module concept from Project Ara](img/b2b2bafdcf7180d12052d20e187a74ed.png)

Camera module concept from Project Ara

如果我告诉你，你的智能手机摄像头是用户可升级的，会怎么样？当下一个伟大的千兆像素传感器出现时，只需弹出该模块，并插入一个新的。如果处理器、屏幕或充电电路也是如此，会怎么样？当然，每个人都想要新的谷歌 Nexus 手机中提供的 USB type-C 快速充电功能。

这听起来很棒，但事实是大多数智能手机用户不知道他们拥有什么。将我们的模块化设计思维导向高端市场是一种失算。想要最高规格的人也想要最薄、最性感的手机。那些已经瘦到了疯狂的地步——iPhone 螺丝[现在有了难以察觉的不同长度](http://hackaday.com/2014/10/19/using-the-wrong-screw-a-painful-lesson-in-iphone-repair/)来解释这种变薄的设计。这些公差使得模块化几乎不可能。

### 标准

![iFixit shows how to replace all of the Nexus 5 "modules"](img/2355154aa240c3456c0f91dc3056aa55.png)

[iFixit](https://www.ifixit.com/Teardown/Nexus+5+Teardown/19016) shows how to replace all of the Nexus 5 “modules”

你可以说我已经有一部模块化手机了。我有一台 Nexus 5，我非常喜欢它，所以我决定不升级到最近发布的 Nexus 5X。相反，我购买了一个替代屏幕(我在一个角落里有一个小芯片 11 个月)，电池和背板。从外面看，这使它成为一个全新的手机，恢复了我的充电时间。所有部件都有连接器，可以轻松更换。

我们真正谈论的模块化智能手机是可以在所有手机的组件之间使用的标准。这包括确定一个物理外形，并确保软件能够处理开发的每个组件。这增加了代码的复杂性，也增加了消除 bug 的难度。对于单一制造商的手机来说，这已经是一个问题，当引入不同公司的模块时，这一问题不太可能得到改善。

目前，谷歌正在开发他们自己的模块化标准，包括框架本身的主动数据处理。Fairphone 的设计使用框架作为基板，每个插槽之间都有导体，这些导体不会主动参与手机的操作方式。

### 有一个顾客

回顾个人电脑革命，很容易想象智能手机的类似道路。我们最终有了主板安装系统的标准，这样机箱就可以与多家制造商相匹配。扩展卡也是如此，它们采用了 [ISA](https://en.wikipedia.org/wiki/Industry_Standard_Architecture) 和后来的 [PCI](https://en.wikipedia.org/wiki/Conventional_PCI) 。这个列表还包括处理器插座、内存插座，甚至那个米色盒子里所有东西的电源连接器。

最后一部分当然是主要问题。谁想要一个米色的智能手机盒子？这些设备是一种身份象征和时尚宣言。成熟的智能手机市场太不稳定，无法广泛采用模块化标准，使手机看起来统一、四四方方等。我并不是说这是不可能绕过的，但在你绕过这个问题之前，你需要建立模块化作为一种成熟的智能手机技术。我认为模块化智能手机的早期采用者将会在发展中国家。

发展中国家的大部分人口没有电脑，他们将会放弃电脑，转而使用智能手机。最初的个人电脑革命忍受了米色的盒子，因为它们很便宜，而且有升级的潜力。我认为模块化智能手机也会出现同样的情况。如果你用 640×480 的摄像头模块代替 4k 视频传感器，可以降低 10%的成本，那你就取得了很大的进步。尤其是如果你以后可以升级那台相机的话。许多低端手机仍然提供的可怜的 8GB 闪存也是如此。这些手机在视觉吸引力方面的不足将通过售后手机保护套来弥补。

在我成长的过程中，我是一个“电脑人”，人们认识我并向我寻求机器方面的帮助。我一次又一次地为老化的机器订购内存升级(同时鼓励所有者尝试 Linux 并从他们老化的马力中获得更多)。我预计，在将模块化智能手机作为第一项互联网技术的人群中，也会出现同样的现象。

### 为什么制造商会接受这一点？

这是一个我无法回答的问题。为什么智能手机制造商愿意走向模块化设计？据我所知，这里只有阻碍因素。Fairphone 是一家初创公司，还没有上市，这并不奇怪。谷歌 Ara 项目的幕后推手——并不是一家硬件制造商。他们是一家广告和内容交付公司，使用 LG 和华为等第三方来制造他们的设备。

为了让模块化设计发挥作用，你需要允许任何人构建模块。这就是为什么我认为我目前的 Nexus 5 与 Fairphone 的工作方式没有什么区别。谷歌为 Nexus 5 生产组件，Fairphone 为他们的手机生产模块。Fairphone 支付了标准的研发费用，你可以打赌他们不会免费提供。如果他们真的允许其他制造商制造模块，肯定会有许可费，这有可能推高成本，削弱这款手机获取发展中国家血汗钱的能力。

有一些方法可以解决这个问题。索尼和微软长期亏本出售游戏机，只是为了用游戏发行商的授权费来弥补。亚马逊新推出的 Kindle Fire 平板电脑售价为 50 美元，但如果你不想在主屏幕上看到广告，你必须额外支付 13 美元。如果其中一个硬件模块是 Google Play 商店，另一个是苹果商店，第三个是亚马逊商店，会怎么样？这些零售商会支付额外费用来独占每部手机吗？

很高兴看到这些概念是怎么回事。但目前我认为它们是更容易维修的手机，而且可能有升级的能力。它们不是模块化的，但随着电子元件的尺寸和成本不断下降，可以想象会有一场模块化手机运动——只要制造商广泛采用像冠军一样工作的明确设计标准。