# 购买前先试一试:3d 打印机

> 原文：<https://hackaday.com/2016/02/22/kicking-the-tires-before-you-buy-3d-printers/>

所以，你想买你的第一台 3D 打印机，你的食指在 Amazon.com 那台 300 美元的打印机上颤抖。停下来。你将会有一段糟糕的时光。3D 打印已经走过了漫长的道路，但大多数 3D 打印机是通过巫术、传说和荒诞的故事设计的，而不是任何严格的工程流程。我会说，大多数 3D 打印机设计要么很糟糕，要么是由中国工程师团队设计的，他们将所有的聪明才智用于削减成本。有几个设计得很好，有一个相对较高的价格标签。

我将从 3D 打印机中出现的一些神话和传说开始。之后，我将介绍一些常见的，主要是噱头的功能，这些功能通常会阻碍你的打印机的能力，而不是增加任何有用的功能。接下来，我将介绍一些能让你的打印机变得更好的东西。最后，如果您是购买第一台打印机的初学者，我将添加一些特殊考虑。

## 神话和传说

大多数打印机的设计在机械方面非常薄弱。你永远不可能在 99.9%的 3D 打印机上扔一个主轴就得到一台数控机床。3D 打印机通常不是为承受负载而设计的，它们不是为处理灰尘而设计的，它们不是为对齐而设计的，或者 CNC 机器所需的任何其他东西。打印机逃脱了大量的机械罪，因为两件事。首先，3D 打印机几乎没有任何负载。第二，除了聊胜于无的位置控制，增材制造不需要任何东西。我的意思是，大多数打印机都很糟糕，但不管怎样，它们还是能工作。

### 轴承 Vs 衬套和其他线性神话

衬套会工作得很好。真的。精密硬化杆上的自润滑套管将非常适合 3D 打印机。与合适的轴承相比，它将同样精确，同样平滑，维护更少，并且不会引起任何问题。大多数 3D 打印机中使用的 LM8EUU 轴承通常具有如此糟糕的公差，可能会降低打印机的精度。

大多数时候，这些都不重要。因为，你的衬套或轴承很可能被推进一片薄薄的 3D 打印塑料里；这将立即否定任一解决方案的任何精度优势。如果一个打印机广告线性轴承或衬套进入钢或铝零件，你可能会得到比另一个打印机选择的精度和刚度优势。否则不太可能。

另一件不会有任何好处的事情是一个普通的 608 滑板轴承骑在一个挤压物上。这些轴承必须预加载，以提供任何精度。它们被设计成吸收一些轴向不对准。为了消除这种轴向错位，必须用弹簧或螺栓对轴承进行预加载，将内圈压向滚珠，然后再压向外圈。两者都必须牢牢把握。如果这种情况没有发生，使用这种方法的 90%的 3D 打印机和 CNC 设计都没有发生，你至少会面临一些错位。这些轴承的好处不会对你的运动精度产生预期的影响。

总之，大多数打印机中的轴承类型不会产生很大的差异，除非它们被适当地限制、加载和对齐；这是很昂贵的。

 [![Most repraps have questionable precision linear bearings pressed into 3d printed plastic and held in place by glue or, more commonly, zip ties. Not very precise.](img/943cd7a18d8b0750ab017285005f1655.png "Reprap Solution")](https://hackaday.com/2016/02/22/kicking-the-tires-before-you-buy-3d-printers/dumbshit/) Most repraps have questionable precision [![The Zortrax M200 has self-lubricating plastic bushings pressed into Metal. A very reliable assembly.](img/2088e19e09d64c381cf5223c6b3e7c7b.png "Zortrax M200")](https://hackaday.com/2016/02/22/kicking-the-tires-before-you-buy-3d-printers/7366d04cb4be58db98fc0a458a23f467_large/) Zortrax M200 has self-lubricating plastic bushings pressed into metal. A very reliable assembly.

### 大型电机与小型电机

对于 3D 打印机来说，NEMA 17 步进电机可能有点大材小用了。它们恰好是最便宜和最容易买到的尺码。大多数 3D 打印机在使用更小、更弱的马达打印时有问题，这是因为它们的设计很差，需要额外的动力。我没有看到许多打印机制造商宣传较小的电机，但一些制造商试图用较大的电机作为升级产品，这是可疑的。

### 同步带、螺钉和细绳等同于弱机械支撑。

如果你想保持低成本，GT2 同步带，甚至低弹力细绳，对你的打印机来说是足够的。即使您有一个精确研磨的 acme 丝杠，并带有适当调整和预加载的丝杠螺母，您仍然不会获得任何优势，除非您正确地握住它们，这是很昂贵的。

这并不是说，如果你有一个等级为 [0 的滚珠丝杠](http://machinedesign.com/mechanical-drives/ball-screw-basics-debunking-myths)在一个适当的地面上，并且是 30 万美元的机械运动的平方，你不会看到更多的精度。这只是说，如果你把一个滚珠丝杠放在你的机器里，并用一个大部分是空心的 PLA 块把它固定住，这是没有意义的。

此外，我会提到，如果选择之间的一点五金店全螺纹和地面或滚动丝杠与铅螺母的任何描述，它绝对，100%，将使您的打印机更准确。特别是对于 Z 轴运动，挤压机或床的重量压在丝杠螺母上，对其进行预加载。

### 注塑塑料部件也好不到哪里去。

![Makerbot used bushings in cheap plastic parts, rendering the steel frame meaningless. http://3Dprinting-blog.com/378-makerbot-replicator-2-upgrade-to-linear-bearings/](img/fb5f8d3e7b1ec159ec2ef10249a2e8bc.png)

Makerbot used bushings in cheap plastic parts, rendering the steel frame meaningless. Photo: [3Dprinting-blog](http://3Dprinting-blog.com/378-makerbot-replicator-2-upgrade-to-linear-bearings/)

Makerbot 用 Replicator 2X 做了这件令人困惑的事情。他们为他们的打印机建造了一个昂贵的钢架，然后用劣质的注塑塑料固定住所有的移动部件。它们是如此的无用，以至于有一大堆的售后市场业务来代替塑料部件。大多数 3D 打印机的主要运动都是由 3D 打印机完成的。这意味着你有一个主要是柔性的材料试图保持刚性。看到问题了吗？它在负载下会弯曲。

一些打印机制造商已经尽力确保承载部件、轴承等。被放在金属里。这些都不是 reprap 打印机。这是没有办法的，不幸的是，物理定律战胜了设计伦理。

## 这些东西可能会让你的打印机体验很糟糕。

### 不超过 3000 美元的打印机上的大床。

你印刷品的第一层是最重要的。有木筏也没关系。错误不会在几层中被去掉。事实是，在你的印刷品的一个较低的层中的任何错误很可能被传送到一个较高的层。所以你必须有一个水平的床。大多数大型打印机都有一个巨大的铝制平板，没有任何公差，依次有三个弹簧，中间有螺钉，支撑电路板，支撑玻璃板，没有任何公差。

你可能会过得很糟糕。对于大多数这些运动，运动越小，你看到的误差就越小。如果一个便宜的杆在 300 毫米上有+-0.5 毫米的直线度误差，你很可能在 300 毫米的末端看到 0.5 毫米，但在 100 毫米上可能只有 0.16 毫米。当你加入所有这些廉价的机制，你开始有一个不可能解决的公差栈。毕竟，你正试图使喷嘴在所有的点上离玻璃板保持 0.18 毫米+/-0.02 毫米的距离。那很难。一台较小的打印机比一台同样价格的大打印机效果更好。自动调平可以弥补这一点。

此外，大型印刷会消耗大量塑料。预计要冒 30-40 美元的风险买一个大的印刷品。

### 奇怪的机制

怪异的机制不会帮助你更好地打印。又来了。你试图精确地、可重复地定位某个东西。每当等式中加入一些东西，就会有更多的东西出错。因此，任何为一种新的创新机制做广告的人，如果没有同时获得工程领域开创性工作的赞誉，很可能是在向你推销一种噱头。如果你喜欢，那很好，但是不要期望你的打印质量会有所提高。很长时间以来，我们一直在设计直线运动的东西。众所周知。

注意:我这里不是在说 delta 打印机，他们专门为 3D 打印机工作，因为 delta 移动不能处理负载，但非常擅长快速、准确的定位。

### 双，三，和其他奇怪的多材料挤出机

这在理论上听起来很神奇，但事实是大多数双挤出机装置在实践中毫无用处。暂停印刷，换灯丝。如果喷嘴之间没有对准；它会毁了你的指纹。如果塑料从一个喷嘴中滴出；它会毁了你的指纹。如果其中一个喷嘴堵塞；它会毁了你的指纹。或者额外的挤压机增加的重量扰乱了你的机械运动。它会毁了你的指纹。可溶解支持在理论上是好的，但它是一个巨大的混乱，其结果是可疑的。你最好用你省下来的钱买一个好的软件，而不是买一个额外的挤压机。

### 蹩脚，廉价，山寨挤出机

挤压机是制造打印机的魔法。对我来说，买一个便宜、质量差的仿制品，然后期望良好的印刷操作，是令人困惑的。再说一次，这里没有聪明的黑客。挤压机做得好不好。我们又回到物理上了。在自动化车床能力方面没有太多巨大的创新。在美国制造它的成本和在中国差不多。因此，除了材料质量和精度，进口挤出机不太可能在任何地方降低成本。买个名牌 [e3D v6](http://e3D-online.com/E3D-v6) 或者 [j 头](http://www.hotends.com/)就行了，或者随便什么做工好有质检步骤的都行。

说真的，这些仿制品如此糟糕，以至于摧毁了 J 形头设计者的精神。他不想再设计了。对于那些买了仿制品的人来说，去坐在角落里想想你都做了些什么。

### 便宜，可怕的组件。

![Circled in red is 3 hours of my life. On the left is my slightly more expensive solid aluminum pulley.](img/328bdefb8b8a7eced5bd0bc34652e68b.png)

Circled in red is 3 hours of my life. On the left is my slightly more expensive solid aluminum pulley.

跟我说，“我无法破解物理。物理学认为我不聪明。要么成功，要么失败。做得好，还是不好”。工程师不是疯子，他们不会伤害你的感情。他们没有囤积秘密，所以他们可以毫无理由地收费。这些都是经过科学检验的真假。这不是一个你可以玩弄的系统，只有一个你可以补偿的系统。

你没有花在好零件上的每一分钱，都是你用来补偿那些便宜零件的时间。比如说。我花了两个小时试图找出为什么我的打印机每隔几层就跳过一些步骤。结果是我买的便宜滑轮出了问题。制造商通过注射成型滑轮齿，并将其压在铝芯上，节省了一些资金。不出意外，塑料牙断了。我从一个有信誉的地方订购了更贵的全铝滑轮，从那以后就没有发生过问题。我买了那些塑料滑轮，可能给自己省了三美元。我最后花了三个小时和额外的十美元来修理一个滑轮。在我看来很傻。

### 笛卡尔打印机上的廉价 Z 轴。

最后，不要买 z 轴便宜的打印机。看起来很死板吗？看起来稳定吗？它看起来像是机器上最贵的机芯吗？如果答案是否定的，跳过它。它的重要性仅次于挤压机。我的打印机有两个家得宝 Z 螺纹杆，同样，我的打印在 Z 上看起来总是很糟糕。不升级就没有办法修复它们。

## 让你的 3D 打印机体验真正精彩的东西。

### 好灯丝。

我们还要重复咒语吗？就像挤压机一样。在一天的开始和结束时，你出去挤出一些塑料。那么，为什么要跑到底部去买你能买到的最便宜的灯丝呢？找一家声誉好的供应商，在你的国家用真正的工程[规格](http://www.taulman3D.com/index.html)制造灯丝，并且只买那种。尝试

![Good Quality Filament on the Right, Cheap Filament on the Left. Both printing at their optimal settings. The good filament print was strong enough to stay together while support material was removed. Don't buy cheap filament.](img/b9ee10d08e8c2b54b98a332f3f816eb0.png)

Good Quality Filament on the Right, Cheap Filament on the Left. Both printing at their optimal settings. The good filament print was strong enough to stay together while support material was removed. Don’t buy cheap filament.

挑选几个品牌，但不要尽可能买最便宜的东西。你会失败的部分，或堵塞你的挤出机，或有一个糟糕的时间。

通常表明优质灯丝的标准是:不圆度误差小于 4%，尺寸公差小于 4%。或者在 1.75 毫米细丝上大约±0.04 毫米。灯丝提到质量检查，激光测微计，和其他昂贵的东西扔在制造过程中。此外，如果该公司可以说出他们的库存颗粒的来源，指向数据表，或给工程规格，这是一个很好的迹象。你不想用回收塑料做灯丝。

此外，最便宜的灯丝通常是黑色的，这是因为你可以研磨任何颜色的塑料，并将其染成黑色。购买便宜的黑色细丝是在你的挤压机里得到一块真正的石头或一点草的好方法。优质黑色灯丝将是原始塑料。

### 刚性和质量

![MakerGear-M2_3D_printer](img/8bc673403abbe979056a9b5569cc7669.png)

The MakerGear M2 has a solid metal frame with precision aluminum plate holding precision rails that are attached to more metal parts. It is heavy, rigid, and likewise, precise.

3D 打印机必须精确定位喷嘴。它还需要以一个合理的速度做到这一点。所以它必须把打印机喷嘴的质量提升到一个速度，然后降低到一个完全相反的速度。力不会消失，它会传递到皮带、滑轮，然后传递到桌子或框架。机器越坚硬，在这样做时弯曲的程度就越小。它还会减少振动，这将减少您的打印效果。这是通过在受力的部分使用不会弯曲的重材料来实现的。如果你的打印机有一个铝挤压框架，但制造商廉价并 3D 打印了将它固定在一起的支架，而不是选择铸造支架，你的打印机仍然会有一些弹性。

此外，当打印机移动时，高得离谱的加固轴会晃动。悬臂也不好。它会出现在你的指纹上。我喜欢 prusa i3 和 printr 机器人，但它们的速度最快。这是一个刚性和对齐的机械噩梦。

### 方形和对齐

这在大多数打印机中是很难做到的。你必须能够使每个轴与另一个轴成直角。或者，就这对你的打印机的实际意义而言，如果你打印一个大的立方体，每个边都应该是完美的正方形。不应该有平行四边形。

大多数打印机不是设计成方形的。如何调整机器是另一天的事情，但现在我建议观看 YouTube 上的一些机械师调整机器的视频，感受一下。这是一门艺术，大多数真实的机器都是为了补偿它而设计的。这就是为什么膝磨机或多或少是为 3D 绘图绘制的纵坐标轴的配置。直觉上很容易理解如何驾驭它。但是，一旦你做了像做龙门磨这样的事情，就变得更加困难了。例如，如果整个框架有点扭曲会发生什么。你会在一头完全是方的，在另一头是方的。

![Delta printers like the Rostock Max V2 from SeeMeCNC won't need as much squaring to function.](img/e8662ac9749c6a1a10be243bc61af1d0.png)

Delta printers like the Rostock Max V2 from SeeMeCNC have different alignment needs.

我要提到的是，对于笛卡尔机来说，这是一个更大的问题，只要轨道相互平行并垂直于机器人的基座，delta 机就可以更容易地补偿这种错位。这些也有一些微妙的对齐。

### 软件中的自动底座调平

如前所述，保持床的水平非常重要。即使在调整好你的机器后，随着时间的推移，你可能仍然会在床上出现一些错位。软件床水平将调整这些小的错位真的很好，使打印更愉快。你仍然希望你的床在喷嘴的 0.5 毫米以内，但是你不再需要花费几个小时来达到 0.01 毫米以内。

### 电子学

这台机器需要一个大脑。如果这个大脑是可靠的，有记录的，设计良好的，有支持的，那就好了。例如，如果机器运行时步进电机电缆中的一根电线断了，该怎么办？(这个奇怪的例子发生在我身上。)如果电路板有保护二极管，没什么大不了的。然而，如果因为一家公司决定通过忽略这一部分来节省每块电路板 25 美分而导致驱动芯片处于无保护状态，那么你也将失去一个驱动芯片。您希望尽可能多地从您的打印机冒险中消除未知因素。电子设备是最复杂的部分。把钱花在他们身上也许是好的。

此外，对于 delta 打印机，像 smoothie-board 这样更强大的板会比基于 Arduino 的更弱的板给你更好的加速。对于 delta 机器来说，数学计算要困难得多。

### 软件

有些人会因为他们的软件精神而不同意我的观点。但是为我的打印机购买更好的软件对我的打印机的改进超过了我的大多数硬件升级。我们正通过一个小孔快速挤压一种非线性流体，它有各种各样奇怪的物理特性。我们的软件设计得越好，我们的印刷品就越好。我的偏好是 simplify3D。我听说其他一些专业解决方案在某些领域超过了它。做研究，做最适合自己的。话虽如此。Slic3r 是一款非常棒的软件，我真的很钦佩它所做的工作。

 [https://www.youtube.com/embed/GHnbkRm9IGg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/GHnbkRm9IGg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



## 初学者

如果你是一个初学者，你可能已经被告知，你可以花 300 美元买一台 3D 打印机，并且某个家伙在他的第八台打印机上说这很容易。你可能有打印那个[小男孩模型](http://prusaprinters.org/3D-print-fallout-4s-pip-boy/)的愿景。嗯，你可以花 300 美元，但需要一段时间才能找到高质量的印刷品。像任何事情一样，合理的花钱会给你带来最好的结果。也不要只买你能找到的最贵的打印机；你最终会得到一个 Makerbot，并且过得更糟糕。做你的研究，检查评论，并检查人们正在打印的部分。

你会得到一些高质量的装备，这会让你的时间过得更好。即文件和支持。

### 证明文件

这是来自 Prusa Research 的官方 Prusa i3 套件的文档。真的很好。当你组装你的第一台打印机时，没有明显的问题会很有帮助。#reprap IRC 频道上的大多数支持问题都来自那些购买了行为怪异的廉价套件的人，或者说不知道哪种方式出现了奇怪的部件。好的文档总是一个公司好工程师和好管理的标志。这是最不有趣的部分，但却是工程过程中最有价值的部分之一。

### 支持

从全球速卖通购买那台深圳复印机，就等于签署了一份免除公司对你可能遇到的产品问题承担任何风险的声明。当电子产品的芯片焊接在背面时，你会怎么做？当你得到一个弯曲的精密杆时，你会怎么做？一个把自己的名字和产品联系在一起的公司需要取悦他们的顾客。

例如，我知道如果一辆[兰博](https://ultimachine.com/content/rambo-13-complete-kit)坏了，Ultimachine 会给它换一辆，几乎不问任何问题。他们会通过电子邮件回复您关于主板的任何问题，并提供量身定制的支持。你能对全球速卖通的[供应商这么说吗？e3D 也一样。如果你对他们的喷嘴有意见，他们会支持你的。这花费了他们的钱。制造不会失败的产品符合他们的最大利益。把钱花在该花的地方。这是我和其他人的经验。这就是为什么 Lulzbot、Prusa 和 SeeMeCNC 都使用这些解决方案，而不是开发自己的解决方案。](http://www.aliexpress.com/wholesale?catId=0&initiative_id=SB_20160210225151&SearchText=rambo+board)

## 已知数量

最后，当购买和制造像 3D 打印机这样复杂的机器时，你几乎肯定会遇到麻烦。所以，你要减少未知的数量，比如问题来自哪里。比如说。如果你有一个不转动的步进电机。如果你从 Ultimachine 买了一块兰博板，你或多或少可以认为这不是那块板的问题。这使得更容易确定它可能是一个连接器，一根电线，一个错误的布线，或电机本身。现在，如果你从易趣上买了 5 美元的马达，那么它可能就是马达。然而，如果你买了一个附带品牌的 Kysan 电机，你也可以排除这种可能性。

这就像在你开始寻找更难的问题之前，检查电脑是否真的插上电源一样。一个便宜的工具包，没有支持，糟糕的机械设计，没有文档，没有可追踪的组件；除了测试每一种可能性之外，没有其他方法可以调试这个问题。

3D 打印机中没有什么神秘的事情发生。然而，你能从中获得的是有限的。这些限制是由真实的物理属性设定的。硬化一根杆需要时间、精力、有经验的人和维护好的机器。这些都要花钱。然而，如果跳过这一步，将会有真实的、可测量的后果。机械工程领域的工作人员非常了解这些后果。所以你的深圳特辑可能会有一些不错的照片。那么线性轴承中的硬化球可能会磨损未硬化杆中的凹槽，并被由此产生的金属粉尘卡住。现实就是这样。这就是为什么一台像样的打印机要 600-2000 美元。

因此，做适当的研究，消除幻想，阅读评论，并购买一台好的打印机。希望你会有一个好的体验，并开始改善你的机器。也许，如果我们幸运的话，你会把你的发现反馈给社区，我们都可以制造更好的机器。