# 打造黑客日超级会议徽章

> 原文：<https://hackaday.com/2017/10/11/building-the-hackaday-superconference-badge/>

再过几周就是最好的硬件大会了。这是 Hackaday 超级会议，为期两天的会谈，额外一天的庆祝活动，烙铁和一个史诗般的硬件徽章。我们已经为这个徽章工作了一段时间，现在终于是时候分享一些早期的细节了。这是一个令人敬畏的徽章，也是如何在极其紧迫的时间表内制造电子产品的一个很好的例子。这是 badgelife，电子会议徽章的硬件演示。

那么，这个徽章是做什么的？这是一架照相机。它有游戏，而且是由迈克电气公司的[迈克·哈里森]设计的。他在一个周末就设计出了这个徽章的原型。板载 PIC32 微控制器、OV9650 摄像头模块和明亮清晰的 128×128 分辨率彩色有机发光二极管显示器。用几个扣子把所有东西绑在一起，你就有了一个真的不可思议的徽章。

那么，你如何得到一个呢？你一定要来 Hackaday 超级会议。今年，我们做的事情有点不同，提前一天开门让黑客村从徽章黑客开始，当晚举行派对，邀请所有来 Supercon 的人！这是一个充满游戏、谜题和视频捕捉的徽章，不容错过。我们还剩不到 30 张票，所以[现在就拿起你的票](https://supercon2017.eventbrite.com/?aff=hadcom1011)继续读下去。

 [![hackadaySuperconferenceBadge-back](img/7aac155a37d47cebe6f79aa47cdd3070.png "hackadaySuperconferenceBadge-back")](https://i0.wp.com/hackaday.com/wp-content/uploads/2017/10/hackadaysuperconferencebadge-back.jpg?ssl=1)  [![hackadaySuperconferenceBadge-front](img/26aff65c2c2dd615cf6c450553d7b696.png "hackadaySuperconferenceBadge-front")](https://i0.wp.com/hackaday.com/wp-content/uploads/2017/10/hackadaysuperconferencebadge-front.jpg?ssl=1) 

### 徽章的起源

由[Voja Antonic]设计的去年的 Supercon 徽章是一件美丽的艺术品。它有比你可以摇动棍子更多的闪光，这个徽章的功能令人惊叹；你只需要四个就能搞定整个会议。

为了今年的徽章，我们联系了 [Mike's Electric Stuff](https://www.youtube.com/user/mikeselectricstuff) 的【Mike Harrison】来设计一个徽章。他是 Hackaday 剧组的好朋友——他负责给 Belgrade 徽章[加伽马校正](https://hackaday.com/2016/04/15/128-leds-5-buttons-ir-comm-and-a-few-hours-what-could-you-create/)的灰度，还做了一个关于[热油高压投影仪](https://hackaday.com/2016/04/19/mike-harrison-exposes-hot-oil-and-high-voltage-of-ancient-live-projector/)的演讲。虽然 x 光机和汞弧整流器更适合[迈克],但我们很有信心他能想出一个有趣的徽章创意。

这个徽章的最初规格是成本约 30 美元，数量约 350 个，面向所有与会者。这给了[Mike]约 1 万美元的预算，并可以自由设计。他带着一些想法回来找我们，第一个想法只是一束由微控制器驱动的白光 led。这将是一个 24×24 的发光二极管矩阵，以及世界上所有的闪光灯。这个想法被拒绝，因为它与其他徽章有点太相似，而且填充巨大的 led 矩阵是一件痛苦的事情。

第二个想法是定制的分段 LCD。是的，就像一个七段或十四段的 LED 显示屏，但带有 Hackaday 徽标，带有一个用于滚动文本或图形的小矩阵。制造一个这样的很容易，因为我们有一台 3D 打印机。建造数百个需要一个工厂。看看阿里巴巴，成本和交货时间看起来是可行的。这个想法被否决了，因为它是一个要么全有要么全无的构建，我们只有一次机会让显示正确。

第三个想法最好描述为“需要一些装配”。这个想法还没有完全具体化，但这个徽章基本上相当于 mecanno 或 snap together 塑料模型套件。每位与会者将获得一个“核心”徽章和几个不同的连接器。这些连接器将在核心之间提供电气和机械连接，最终在超级大会期间，在一个大众制造的 Voltron 机器人中达到高潮。

理智占了上风，我们最终选定了今年徽章的设计。这将是一个摄像头，依靠易贝极其便宜的 SPI 摄像头模块。混合了 64k 内存和 256k 闪存的 PIC32，一个大有机发光二极管显示器和一个 SD 卡插座，我们有一个很好的会议徽章硬件计划。一点点改进——以及 Microchip 捐赠的部件——添加了一个串行 SRAM，使相机可以捕捉 QVGA 分辨率的图像。

### 让我们从易贝单一来源。那太好了

我们有一个原型，我们有订单上的大部分 BOM，就在我写这篇文章之前，我点击了 Macrofab 网站上漂亮的绿色按钮开始订购。生产现在已经开始，但是我认为谈论已经出现的一些问题是重要的。

[![](img/4c556a8cb05452da165c9b2dcd2a5fac.png)](https://hackaday.com/wp-content/uploads/2017/10/cameramodules.jpg)

The precious camera modules

该徽章的供应链和 BOM 管理非常简单。当然，电池座有点奇怪。(有人能告诉我电池座是怎么回事吗？在任何项目中，它们都是最难找到的组件。)我们用于相机闪光灯的 LED 需要一些组装工作，但大多数零件都是标准的，容易采购的组件，到处都有大量库存。相机模块和有机发光二极管显示器不是。这些来自全球速卖通和易贝。在全球速卖通有几家显示器供应商，但相机模块在全世界只有一家供应商:易贝只有一家。

这个 OV9650 相机模块在易贝展出。这是一个相对古老的相机模块，但它在 [Arducam](http://www.arducam.com/) 社区中确实有很多用途。它是 130 万像素，非常便宜，当我开始这个项目时，[Mike]已经为相机设计好了所有的寄存器。我们唯一要做的就是买 500 个。不是问题；易贝的列表显示，他们已经卖出了数百件，还有“10 多件可用”。让我们从易贝单源。会很棒的。

在下了 8 卷 70 台相机的“立即购买”订单后，卖家回复了我。他们只有 35 个。不，不是三十五卷七十架相机；三十五个*共*。

此时，我们有几个选择。易贝卖家有几个其他模块，“它们的外观与易贝上的不一样”。该模块可能适用于当前版本的徽章，也可能不适用于当前版本的徽章，因此一些样本很快被发送到英国的[Mike]。第二种选择是从全球速卖通采购类似的兼容相机模块[。这个计划的问题是易贝相机的价格大约是 2 美元。全球速卖通相机价值 13.50 美元。考虑到这个徽章的 BOM 已经是 25 美元，这将超出预算。这是一个会议徽章，我们无论如何都要做，但这将是一个可怕的选择。](https://www.aliexpress.com/item/Free-shipping-OV9650-9650-1-3-million-pixels-camera-module-OV9650-camera-module-with-FPC-connector/32594782307.html)

第三种选择是完全使用另一个相机模块。OV7670 相机模块非常丰富，使用与我们正在使用的模块相同的 FFC 连接器，如果您查看 Arducam 库，看起来我们不会失去所有的 NRE。这款相机的缺点是分辨率为 640×480。不理想，但它会工作。

经过一两周与易贝卖家的反复沟通，并向[Mike]发送了一些样品相机，我们最终有了一个可行的解决方案。“外观不同”的 OV9650 摄像机也能工作。他们没有什么真正的不同；FFC 连接器有点长，镜头螺丝的形状略有不同。尽管如此，我们还是损失了一周的开发时间，从易贝单一采购。

### 现在轮到你黑徽章了

世界上没有其他会议像 Hackaday Supercon 这样做徽章黑客。需要证明吗？为了 2015 年的会议，[人们将一点玻璃纤维](https://hackaday.com/2015/11/20/the-best-conference-badge-hacking-youve-ever-seen/)变成了调幅收音机、布谷鸟钟和一个基本的神经系统。[甚至还有火花隙](https://hackaday.com/2015/12/09/the-best-badges-of-the-supercon/)，如果再多一点时间，就会有特斯拉线圈了。请记住，2015 年的 Supercon 徽章只是一个空白的 PCB。

2016 年，我们给了 Supercon 与会者更多的机会。去年的 Supercon 徽章是一个由 128 个 led 组成的阵列，几个按钮，一个加密挑战，以及令人惊讶的小原型区域。尽管如此，[【扎克·弗雷丁】还是设法把徽章](https://hackaday.com/2016/11/21/showing-off-the-badge-hacks-from-supercon/)钉在了一块覆铜板上。[雷霆之声]把她的徽章和几个纸盘[变成了一个扬声器](https://hackaday.io/project/18303-hackaday-2016-paper-plate-badge-hack)。[Sprite_tm]是一个成功者，成功地用四个徽章征服了超级观众[。没有任何一次会议像这次会议这样严肃地对待徽章黑客行为，其结果也是如此惊人。](https://www.youtube.com/watch?v=43ErQc-u9wA&t=28m52s)

今年也不例外，我们会给每个人一个好的开始。我们希望有人——任何人——带着准备好的扩展板到达会场。我们希望看到这个徽章独立的“盾牌”。这应该会为您的起步提供一些提示:

[![](img/0304f608e313403d98cd51a799ec090f.png)](https://hackaday.com/wp-content/uploads/2017/10/cambadge.png)

The 2017 Hackaday Superconference badge. Top silk, pads, and outline visible. Have fun.

这就是了。这是你的挑战。我们希望在任何地方都能看到最好的徽章黑客*，现在是你站出来的时候了。我们将很快发布全部细节，包括一些机械图纸和一些固件*，但徽章正在制作中，现在球在你的球场上。给我们看看你有什么，因为这是我们做过的最好的徽章。**

 *** * *

立即购买您的 [Hackaday Superconference 入场券](https://supercon2017.eventbrite.com/?aff=hadcom1011)。

* * ***