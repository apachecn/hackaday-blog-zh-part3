# 电子文本春假解决信号阻断、音频生成和无线电传输问题

> 原文：<https://hackaday.com/2018/04/20/e-textiles-spring-break-tackels-signal-blocking-audio-generation-and-radio-transmissions/>

寻找电子纺织品的杀手级应用是黑客的领域，在这个领域里，任何事情都有可能发生。无论是通过信号屏蔽保护你的数字隐私，还是通过可穿戴的 BeagleBone 或 555 定时器产生音频，或者将你最喜欢的衣服制成天线，eTextile Spring Break 都在尝试将电子产品和织物结合起来的方法。

你可能会问自己“电子纺织品有什么用途？”。嗯，这是一个很好的问题，也可能是当今行业面临的最常见的问题。恐怕我无法给出一个明确的答案。作为一名电子纺织品从业者，我也经常问自己这个问题。穿在身上的织物和我们的电子设备有一种固有的个人性质，这使得这个答案难以捉摸。我不是试图编造一些狭隘的定义，而是通过最近在纽约举行的为期一周的活动 [eTextile Spring Break](http://etextilespringbreak.org/) 来审视感兴趣的主题、材料实验和技术探索。

## 纺织春假

在市场的影响之外，法国农村每年都会举行一次特殊的活动。在这里，电子纺织品从业者和羊毛朋克们聚在一起讨论，在导电纤维和大量葡萄酒中创造。这个活动叫做[电子文本夏令营](http://etextile-summercamp.org/)。eTextile Spring Break 是 SummerCamp 的衍生产品，它在美国培育了一个围绕电子纺织品的社区。我有幸与[和另外三名女性](http://etextilespringbreak.org/home/)共同组织了这次活动，我将分享我作为组织者和参与者四处奔走时所看到的一些工作。

## 作为表演管道和声音产生的电子纺织品

电子纺织品可以成为实验仪器设计的有趣解决方案，并为表演者和非表演者提供有趣的输出。从技术上来说，当你想要创作一首音乐作品时，有很多制造噪音的选择。eTextile Spring Break 的两个研讨会涵盖了一个高科技选项，而另一个则涵盖了相对较低的技术选项。

### 衣服上的喙骨

[![](img/7618f8fe552162bdbb4befb20e7b60e8.png)](https://hackaday.com/wp-content/uploads/2018/04/bela-fcbv0-2-becky-stewart.jpg)

Bela on fabric FCB breakout with snap connectors. Photo by Becky Stewart.

Becky Stewart 在一个名为[音频处理简介](http://etextilespringbreak.org/intro-to-audio-processing-with-bela/)的研讨会上教授了 [Bela](http://bela.io/) ，这是一个专门为超低延迟音频处理设计的平台。Bela 将基于浏览器的 IDE 与 BeagleBone Black 的 cape 结合在一起。这里展示了这种硬件的最新版本。这个板子叫做[贝拉迷你](https://blog.bela.io/2018/02/22/bela-mini-launch/)，是小猎犬的盾牌。

Becky 与 Sophie Skach 和 An Liang 合作，正在建立一个名为 Embelashed 的可穿戴原型平台。该系统包括用于 Bela 的基于织物的控制板、由导电和电阻织物制成的拉伸传感器和开关，用导电织物连接部件。

研讨会讨论了 IDE 中包含的 C++示例和纯数据补丁，以及 Becky 专门为可穿戴应用程序创建的一些纯数据补丁。您可以查看 Embelashed repository 上的 wiki，了解研讨会期间介绍的[更多示例。如果你想更多地了解上图所示的连接结构，贝基也有](https://github.com/theleadingzero/embelashed/wiki/Generating-Genius-Workshop-February-2018)[一张带标签的图片](https://github.com/theleadingzero/embelashed/blob/master/hardware/fcb/classic/fbc-wired-connectionsv0.2.png)。

 [![Playing music with a knitted stretch sensor made by Becky Stewart in her Sound Processing with Bela workshop.](img/803d6db31d0c1a0b221b4392810393f8.png "bela_stretch")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/04/bela_stretch.jpg?ssl=1) Playing music with a knitted stretch sensor made by Becky Stewart in her Sound Processing with Bela workshop. [![Bela browser-based IDE. Photo by Afroditi Psarra.](img/94c610eb9103aa20f790982d4cb09788.png)](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/04/bela_afroditi.jpg?ssl=1) Bela browser-based IDE. Photo by Afroditi Psarra. [![Me wearing the Embelashed Bela wearable platform. Two e-textile stretch sensors on the elbows controlled pitch and delay. A top switch adds reverb. Photo by Rachel Drozdowicz.](img/433c5123ee6b2edea88bca67af937828.png "Bela_rachel_d")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/04/bela_rachel_d.jpeg?ssl=1) Me wearing the Embelashed Bela wearable platform. Two e-textile stretch sensors on the elbows controlled pitch and delay. A top switch adds reverb. Photo by Rachel Drozdowicz.

### 通电和数控切割电路

Martin De Bie 和 Adrian Freed 领导了一个[研讨会](http://etextilespringbreak.org/e-textile-sound-and-music/),围绕使用微控制器和 555 定时器 IC 的声音生成和操作。

 [![V2.1](img/c7382f28c089523a993a31a9e0710190.png "V2.1")](https://hackaday.com/2018/04/20/e-textiles-spring-break-tackels-signal-blocking-audio-generation-and-radio-transmissions/v2-1/)  [![Left: The first generation of the breakout taught in the workshop. Image by Martin De Bie. Right: The third cut from copper foil, soon to be conductive fabric. Photo by Adrian Freed.](img/c1cac1d8bed756dd29bd09f31c3fb151.png "Adrian_sidebyside")](https://hackaday.com/2018/04/20/e-textiles-spring-break-tackels-signal-blocking-audio-generation-and-radio-transmissions/adrian_sidebyside/) Left: The first generation of the breakout taught in the workshop. Image by Martin De Bie. Right: The third cut from copper foil, soon to be conductive fabric. Photo by Adrian Freed.

马丁为他和阿德里安开发的 555 领导了一个熨烫导电织物分线点的建设。该电路设计有交叉垫，允许您将手指放在 555 定时器振荡器电路中电阻通常所在的位置。在春假期间，Martin 和 Adrian 对电路设计进行了几次迭代。CNC 使用[剪影浮雕](https://www.silhouetteamerica.com/shop/machines/cameo)从导电织物和铜带切割每一次迭代。在[马丁](https://github.com/WhiteDileckNoise/hardware/tree/master/textiloV2)的 Github 和[阿德里安](http://adrianfreed.com/content/textile-555-oscillator-electrosomatophone-circuit-bending)的网站上阅读更多关于他们设计的内容。

## 用电子纺织品屏蔽信号

[![](img/03a9428f76b0733994b7756cfd9f329a.png)](https://hackaday.com/wp-content/uploads/2018/04/irene_liza.jpg)

Liza and Irene speaking about their mesh shields and Faraday garment with embedded induction coil circuit.

我们生活在一个互联设备使用无线电波无线传输数据的世界。手机很少关机，设计用于发射和接收的收音机出现在各种消费产品中。这些辐射关系到人们，不仅是因为围绕它们是否会造成身体伤害(放射病)的争论，还因为监测问题的出现。在所有这些连接的设备之间传递的是什么信息？作为对比，我们是否可以阻止来自传入传输的潜在入侵，这些传输会触发从设备传出的不必要的个人数据突发？

作为软世界中的硬隐私焦点小组的一部分，Liza Stark 和 Irene Posch 研究并探索了通过设计导电纺织品图案来阻挡无线电波的方法。他们制造的受法拉第笼启发的样本仍处于测试阶段，在活动结束时还没有发挥作用。尽管如此，这些图案是引人注目的，由阻挡辐射的必要性所驱动的美学概念也是耐人寻味的。

 [![sheilds_irene](img/9ba6863f4b3bd29d95cc6cb54fa2870e.png "sheilds_irene")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/04/sheilds_irene.jpg?ssl=1)  [![shields2_irene](img/45a0128fcfaa01506e86711d97587f30.png "shields2_irene")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/04/shields2_irene.jpg?ssl=1) [![](img/ef9912d44bb4a390a6fe8609512fe108.png)](http://hackaday.com/2018/04/20/e-textiles-spring-break-tackels-signal-blocking-audio-generation-and-radio-transmissions/induction_irene_small/)

Lighting up an LED by bringing one coil built into a handpiece closer to the second coil embedded in the shoulder of the garment. Photo by Irene Posch.

Liza 和 Irene 还探索了可视化无线能量传输的概念。随着手的一挥，他们点亮了衣服上的 LED，将能量从一个感应线圈传输到另一个。这说明了当外部信号指向你时被通知的概念。想象一下，在未来，你的穿着会对附近的杂散射频做出反应。

电路的驱动端被嵌入到一件设计成一个大法拉第笼的衣服中。被设计成可以拉上全身的拉链来保护自己免受无线电波的伤害。宽大的剪裁和实用的口袋给人一种游牧的感觉。

## 体内平底锅和可佩戴天线

无线传输在电子纺织春假期间继续保持强势。与会者带来了关于电子纺织品天线的最新研究，并针对各种带宽构建了新的天线以及发射器和接收器电路。

### 调频无线电发射机和导电纤维天线

[![](img/cbf2226805710ab58174267fe73e75c4.png)](https://hackaday.com/wp-content/uploads/2018/04/revel3_afroditi.jpg)

Sam trying on the wearable FM receiver antenna made by Afroditi. Photo by Afroditi Psarra.

[Revel off the Grid](http://etextilespringbreak.org/revel-off-the-grid/) 焦点小组构建了一个 DIY 通信网络，包括 FM 和 AM 发射器、接收器和基于纺织品的天线。所有可穿戴天线都是基于保罗·内帕和亨德里克·罗吉尔的研究论文中的[之前的设计。论文中的](http://chrome-extension://oemmndcbldboiebfnladdacbdfmadadm/https://biblio.ugent.be/publication/7045516/file/7045521)[偶极](https://en.wikipedia.org/wiki/Dipole_antenna)和[螺旋](https://en.wikipedia.org/wiki/Helical_antenna)天线设计使用导电织物和线制作成可穿戴天线。第一个是由 Afroditi Psarra 创造的对称四指设计，她自己做了大量的[天线研究](http://afroditipsarra.com/index.php?/on-going/fractal-antennae/)。

这个四指天线连接到一个 FM 接收器上，这个接收器是在 Wassaic 项目的一个架子上找到的。第二种天线设计用于两个使用 555 定时器构建的 FM 发射器。它们由一个用直[地网](https://www.smeter.net/grounds/tuned-counterpoise-grounds.php)平衡的线圈组成，信号馈入位于中间。Sam Topley 是该小组的五名成员之一，她决定通过混合中性和导电纱线和线来创建一个导电的 pom-pom 天线(见下文),从而打造自己的道路。

天线不是唯一得到电子纺织品待遇的东西。Nicole Messier 和 Sam 分别用 CNC 切割的烫印导电织物和手工缝制的导电线制作了他们的发射器电路。“脱离网格狂欢”焦点小组的探索以某种形式的表演达到高潮。当佩戴者在寻找最强的信号时，可佩戴天线提供了运动的动力，因为手动内置的 FM 发射器电路向 FM 接收器发送脉冲麦克风输入。

 [![Sewn FM transmitter circuit with pom-pom antenna. Created by Sam Topley. Photo by Teresa Lamb.](img/a0abc456d5144850b414d32faaafcb7e.png "revel4_teresa")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/04/revel4_teresa.png?ssl=1) Sewn FM transmitter circuit with pom-pom antenna. Created by Sam Topley. Photo by Teresa Lamb. [![Nicole's helical sleeve antenna and conductive FM transmitter circuit.](img/4d11f26b7b7f61eedcd6efff6a2dc492.png)](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/04/revel1.jpg?ssl=1) Nicole’s helical sleeve antenna and conductive FM transmitter circuit. [![My sleeve antenna with FM transmitter circuit attached to the inside of a mask to catch vocal transmissions.](img/cd97471a05a34f51f40f5e5e58991e9c.png)](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/04/off_grid.jpg?ssl=1) My sleeve antenna with FM transmitter circuit attached to the inside of a mask to catch vocal transmissions.

### RFID 和个人局域网

[![](img/9e575224ff3f3c665780044f35690c1e.png)](https://hackaday.com/wp-content/uploads/2018/04/rfid1.jpg)

RFID fabric circuit with an antenna built during Nicole and Ingo’s workshop.

由 Nicole Messier 和 Ingo Randolf 领导的研讨会讨论了 RFID 和近场体内通信设备等无线技术。Nicole 引导学生通过一个 RFID 发射器电路和天线，该电路和天线用于 Adafruit 的 PN532 NFC/RFID Arduino 屏蔽。

Ingo Randolf 向学生展示了如何构建接收器和发射器电路，以便通过电容耦合在人体中传输数据。这些电路是基于托马斯·格思里·齐默曼在 1995 年写的一篇论文。它是如何工作的？以下是摘自齐默曼论文的概要:

> “近场体内 PAN(个人区域网络)是一种无线通信系统，它允许人体上和附近的电子设备通过近场静电耦合来交换数字信息。信息通过调制电场和将皮安电流静电(电容)耦合到体内来传输。身体将微小电流(例如 50 pA)传导至安装在身体上的接收器。环境(“房间接地”)为传输信号提供了返回路径。使用低频载波(例如，330 kHz ),因此没有能量传播，从而最小化远程窃听和相邻 pan 的干扰。使用类似 RS232 的简单串行数据协议，通过开关键控来传输数字信息。”

[![](img/d97ac5f1c34da01a338331e62eea7b3b.png)](https://hackaday.com/wp-content/uploads/2018/04/pan_irene.jpg)

Ingo testing how many bodies the circuit can take before the data is sent. Photo by Irene Posch.

Ingo 在他的网站上提供了电路图和代码，并指出它在设计电子纺织品和可穿戴电子产品时的用处:

> “利用身体作为交流渠道是一种有趣的方式，可以将传感器数据从身体的一个部位发送到身体的另一个部位，或者发送到另一个身体。这可能对电子纺织品项目非常有用。尤其是当不可能使用导电材料来传输数据时。”

## 建立一个电子纺织品社区

eTextile 春假不仅仅是培养一个从业者社区。这也是关于在我们都回家后去接触社区。在周末，eTextile 春假社交向公众打开了 Wassaic 项目的大门。在活动中，人们阅读了展示的参与者的作品，包括一周内创作的作品。有研讨会和活动，如与 Audrey Briot 和 Martin De Bie 一起编织 Ur Face，与 Ingo Randolf 一起针刺制毡，以及与 Pauline Vierne 和 Sasha de Koninck 一起使用热变色和光致变色油墨进行丝网印刷。

 [![Knitting my face.](img/dd1fb49f8cc5f922d8a91d418a04c86f.png "OLYMPUS DIGITAL CAMERA")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/04/kniturface2.jpg?ssl=1) Knitting my face. [![Screen printing with Pauline.](img/af224a1d2a5809494cd8141931d1fb8c.png "OLYMPUS DIGITAL CAMERA")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/04/social1_screen.jpg?ssl=1) Screen printing with Pauline. [![Needle felting with Ingo.](img/35af48e54e5869dad7a5ba4ec74fa264.png "OLYMPUS DIGITAL CAMERA")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/04/social3_felting.jpg?ssl=1) Needle felting with Ingo. [![Pauline ponders what wicked fabrics she will work with next.](img/a9f7d3f9ee337b99f6d8b16f4302ca4a.png "IMG_1887")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/04/img_1887.jpg?ssl=1) Pauline ponders what wicked fabrics she will work with next.

我了解到，电子纺织品可以降低那些通常会被恐吓或劝阻学习电子电路构建的人群(如妇女和年轻女孩)的准入门槛。它用传统工艺强化工程原理，在意想不到的人群和兴趣之间架起桥梁。电子纺织品是新旧技术的完美结合，在你意识到之前，你可能正在学习如何一边编织一边制造噪音音乐。

[![](img/459061b3298fa22902152cf8c8f73f2d.png)](https://hackaday.com/wp-content/uploads/2018/04/social_knittingnoise.png)

Sam Topley showing a young visitor how to knit and make noise using her SNOG sound generating circuit.

[主要图片来源:[山姆·托普雷](https://twitter.com/samtopley/status/982352505639088128)