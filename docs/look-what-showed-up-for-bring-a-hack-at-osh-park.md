# 看看什么出现在奥什公园

> 原文：<https://hackaday.com/2016/10/15/look-what-showed-up-for-bring-a-hack-at-osh-park/>

Hackaday 上周末在波特兰参加了开放硬件峰会。本周早些时候，我做了一个简短的回顾，但是这篇文章一直在我的脑海里。在峰会的前一天晚上，OSH Park(我们都知道和喜爱的完美紫色 PCB 的供应商)在他们的总部举办了一场黑客大会。[Laen]知道如何举办派对——提供所有人都喜欢的宴会和开放式酒吧。这个地方挤满了令人敬畏的黑客，每个人都有一些惊人的东西可以炫耀。

事实上，有太多的人在炫耀硬件，我无法在一个晚上全部捕捉到。但是在跳完之后，请和我一起分享六七个非常突出的例子。

 [![APA102 LEDs driven by Photon](img/9901e5d670048a3d94d263bab718aefb.png "0101-louisbeaudoin-particle-apa102")](https://hackaday.com/2016/10/15/look-what-showed-up-for-bring-a-hack-at-osh-park/0101-louisbeaudoin-particle-apa102/) APA102 LEDs driven by Photon [![Particle Photo on the host board](img/e9ff6a5d53c2db352dffdef75c8331d2.png "0102-louisbeaudoin-particle-driverboard")](https://hackaday.com/2016/10/15/look-what-showed-up-for-bring-a-hack-at-osh-park/0102-louisbeaudoin-particle-driverboard/) Particle Photo on the host board [![View of host board -- headers underneath](img/0c2ee1af419b168b1d87608de0d7def6.png "0103-louisbeaudoin-particle-hostboard")](https://hackaday.com/2016/10/15/look-what-showed-up-for-bring-a-hack-at-osh-park/0103-louisbeaudoin-particle-hostboard/) View of host board — headers underneath [![cool SMD through-hole headers](img/945bd9b3a7379eca1ced2cba9ab0e1a9.png "0104-louisbeaudoin-particle-through-headers")](https://hackaday.com/2016/10/15/look-what-showed-up-for-bring-a-hack-at-osh-park/0104-louisbeaudoin-particle-through-headers/) cool SMD through-hole headers

在过去的几年里，我们到处都能碰到路易斯·博多因。他是我在我的 [1 像素吃豆人](https://hackaday.com/2015/06/01/1-pixel-pacman/)项目中使用的 [SmartMatrix](https://hackaday.io/project/5900-smartmatrix-led-art-display-and-music-visualizer) 的幕后推手。他带来了一个基于粒子光子(一个 WiFi 开发板)的项目，该项目驱动 APA102 LEDs。你可以[看看他正在开发的软件](https://github.com/pixelmatix/SmartMatrix-Photon-APA102)，但是光子的分线板吸引了我的眼球。Photon 上的引脚头似乎插入了 0.1 英寸间距的原型板。在底部，您可以看到一组表面贴装接头，允许通孔直接通过。酷！

 [![Commodity heads-up glasses are expandable](img/9f7eab67d23ec45a51cc97207e1d6f09.png "0701-shea-ivey-laforge-fpv-overlay")](https://i0.wp.com/hackaday.com/wp-content/uploads/2016/10/0701-shea-ivey-laforge-fpv-overlay.jpg?ssl=1) Commodity heads-up glasses are expandable [![The expansion module](img/32c8eb49cdb5b92b57828d74c51e44c4.png "0702-shea-ivey-laforge-fpv-overlay")](https://i0.wp.com/hackaday.com/wp-content/uploads/2016/10/0702-shea-ivey-laforge-fpv-overlay.jpg?ssl=1) The expansion module [![Video overlay demo](img/361db4124bbfd2040b41c90734b8b36f.png "0703-shea-ivey-laforge-fpv-overlay")](https://i0.wp.com/hackaday.com/wp-content/uploads/2016/10/0703-shea-ivey-laforge-fpv-overlay.gif?ssl=1) Video overlay demo

这里有一些针对 FPV 钢筋混凝土现场(想想四轴飞行器比赛之类的)。谢伊·艾维正在开发模块来扩展胖鲨遥控视觉眼镜的功能。这些头戴式显示器上有一个扩展端口。他正在演示的模块连接到四轴飞行器上的摄像头输出(这是一个超小的板，这里没有画出)，可以在显示器上覆盖任何你想要的信息——指南针，海拔高度，电池等。该模块本身有一个屏幕和用户控制，用于选择您想要使用的设置。

 [![An ODB-II](img/791c448726b500c95f2d323aae5acbda.png "0501-josh-sharpe-macchina-can-tool")](https://i0.wp.com/hackaday.com/wp-content/uploads/2016/10/0501-josh-sharpe-macchina-can-tool.jpg?ssl=1) An ODB-II [![Two boards stack on one another](img/c0fbb88b99469e004487ce6533fa3e61.png "0502-josh-sharpe-macchina-can-tool")](https://i0.wp.com/hackaday.com/wp-content/uploads/2016/10/0502-josh-sharpe-macchina-can-tool.jpg?ssl=1) Two boards stack on one another [![ESP32 in the ZigBee header](img/d6c21e5a9cccb2c7a4e00309547051fe.png "0503-josh-sharpe-macchina-can-tool")](https://i0.wp.com/hackaday.com/wp-content/uploads/2016/10/0503-josh-sharpe-macchina-can-tool.jpg?ssl=1) ESP32 in the ZigBee header [![What's in between the boards](img/d1ef0e67c1bb96ff0954a6e08bea81c6.png "0504-josh-sharpe-macchina-can-tool")](https://i0.wp.com/hackaday.com/wp-content/uploads/2016/10/0504-josh-sharpe-macchina-can-tool.jpg?ssl=1) What’s in between the boards

我第一次遇见[Josh Sharpe]是在去年的 CES 上，很高兴在这次聚会上再次见到他。他的公司正带着汽车黑客的梦想走向发布。它插入 ODB-II 端口，有各种各样的好东西，如 SD 卡插槽和装载了 ESP32 的 ZigBee 头。[Josh]不是在 ESP32 上跑罐；他有一个收发器，最新最棒的蓝牙+WiFi 芯片就是这个——一个 WiFi 和蓝牙接口。他炫耀的红色板子超级有趣；这是我第一次在野外看到 ESP32，它不是我们以前遇到的开发板之一。

 [![PCB panel cruft for recycling](img/631d291c6f23e0ca4b64492fa6f44af4.png "0601-osh-park-recycling")](https://hackaday.com/2016/10/15/look-what-showed-up-for-bring-a-hack-at-osh-park/0601-osh-park-recycling/) PCB panel cruft for recycling [![Burger King ain't got nothin' on this crown.](img/25a8caececa80f6659e9b07d3d631236.png "0602-osh-park-crown")](https://hackaday.com/2016/10/15/look-what-showed-up-for-bring-a-hack-at-osh-park/0602-osh-park-crown-2/) Burger King ain’t got nothin’ on this crown.

在奥什公园，他们旋转多氯联苯面板，然后将它们分开，运送给许多不同的客户。这意味着来自面板边缘的废料和不能被“俄罗斯方块”到有用空间的东西。我喜欢他们在聚会前没有扔掉他们的回收品，因为看到这个巨大的废物箱令人印象深刻。

有一吨的奥什公园板展出，但这个皇冠对我来说似乎特别可怕！

 [![Internet of Fuzzy Dice](img/6476603b30724f97ecb3052c80164928.png "0201-scott-dixon-internet-of-fuzzy-dice")](https://hackaday.com/2016/10/15/look-what-showed-up-for-bring-a-hack-at-osh-park/0201-scott-dixon-internet-of-fuzzy-dice/) Internet of Fuzzy Dice [![What's in each die](img/c935310637668777139b509cf9560a89.png "0201-scott-dixon-internet-of-fuzzy-dice-pcb")](https://hackaday.com/2016/10/15/look-what-showed-up-for-bring-a-hack-at-osh-park/0201-scott-dixon-internet-of-fuzzy-dice-pcb/) What’s in each die

来见见[斯科特·狄克逊]带到派对上的模糊骰子网络。他们使用 Rigado [BMD-200 模块](https://rigado.zendesk.com/hc/en-us/sections/205098027-Previous-modules)将骰子连接到显示器。掷骰子，产生的正面将会显示在显示器上，这个显示器位于一个重新设计的外壳中，看起来很棒！

 [![The brain board](img/a14501e5ef301d07a46ff770b815c80c.png "0801-zach-fredin-pov-watch-overview")](https://hackaday.com/2016/10/15/look-what-showed-up-for-bring-a-hack-at-osh-park/0801-zach-fredin-pov-watch-overview/) The brain board [![Yes, those are LEDs!!!](img/f22a27e8a703a2561d52a488649f45b4.png "0802-zach-fredin-pov-watch-leds")](https://hackaday.com/2016/10/15/look-what-showed-up-for-bring-a-hack-at-osh-park/0802-zach-fredin-pov-watch-leds/) Yes, those are LEDs!!! [![The battery board](img/f4c62d12d94475e0cd1e6a8da57d9706.png "0803-zach-fredin-pov-watch-battery")](https://hackaday.com/2016/10/15/look-what-showed-up-for-bring-a-hack-at-osh-park/0803-zach-fredin-pov-watch-battery/) The battery board [![In action](img/d98b545f31b8a230fe73a597223ea214.png "0804-zach-fredin-pov-watch-pandering")](https://hackaday.com/2016/10/15/look-what-showed-up-for-bring-a-hack-at-osh-park/0804-zach-fredin-pov-watch-pandering/) In action

你可以发现[Zack Fredin]经常以[zakqwy]的名字在 Hackaday.io 上闲逛。他是[neuro bytes](https://hackaday.io/project/3339-neurobytes)(2015 年 Hackaday 奖最佳产品决赛选手)背后的头脑。看看他所谓的“周末新奇项目”——[这款 POV 腕表](https://hackaday.io/project/8160-weekend-novelty-projects)配有一组非常密集的手工焊接 SMD LEDs。哇！

当他来回扭动他的手腕时，我无法很好地拍摄显示器，但用眼睛很容易辨认出来。这里的图片来自他的项目页面。腕带是带有 JST 连接器的电线。有三块板，大脑板托管一个 Teensy 3.2，LED 板使用 SPI 驱动的移位寄存器，底部的电池板有点黑在一起，只是为了真正赢得我们的心。这是一个史诗般的建筑，在他的页面上给他一个赞吧！！

当你在那里的时候，看看他用覆铜快速成型的技术。飞机被 X-ACTO 刀切割成碎片。这很有趣，任何将参加[黑客日超级会议](https://hackaday.io/superconference/)的人都应该找到他——他将帮助领导徽章黑客活动，我打赌我们可以说服他就这项技术举办一些小型研讨会。

 [![0301-cosmoneer-satellite-learning-kit](img/78d245f6090796de9285e9635b470556.png "0301-cosmoneer-satellite-learning-kit")](https://hackaday.com/2016/10/15/look-what-showed-up-for-bring-a-hack-at-osh-park/0301-cosmoneer-satellite-learning-kit/)  [![0302-cosmoneer-satellite-learning-kit](img/d71021d06e66e079a91a024ab114a2be.png "0302-cosmoneer-satellite-learning-kit")](https://hackaday.com/2016/10/15/look-what-showed-up-for-bring-a-hack-at-osh-park/0302-cosmoneer-satellite-learning-kit/) 

这个叫做[宇宙工程师](http://www.cosmospioneering.com/)的很酷的小工具即将进入众筹。它试图让孩子们对立方体卫星感到兴奋。你组装好工具包，用一根小线把它挂起来，然后用一个充当飞轮的马达来展示它们在绕地球旋转时是如何改变方向的。在这个演示中，天平是通过增减硬币来校准的，能量是通过无线传输的。有一堆不同的有趣的概念，其中肯定有一个会让一个中学生头脑发热。

 [![Eric Pan showing ReSpeaker detecting directional audio](img/6e35d8d809ca729028079a0247098fb1.png "0401-eric-pan-respeaker")](https://hackaday.com/2016/10/15/look-what-showed-up-for-bring-a-hack-at-osh-park/0401-eric-pan-respeaker/) Eric Pan showing ReSpeaker detecting directional audio [![Six microphones around the outside](img/c42ab97abd4df797fa61479aa3af4fa1.png "0402-eric-pan-respeaker")](https://hackaday.com/2016/10/15/look-what-showed-up-for-bring-a-hack-at-osh-park/0402-eric-pan-respeaker/) Six microphones around the outside

Seeed Studio 的首席执行官(CEO)埃里克·潘(Eric Pan)带来了一块新的演讲板。它运行了一个小程序，根据声音的来源照亮了电路板的不同面。在与他谈论这件事的过程中，我开始对这块板的潜力感到非常兴奋。例如，他提到它有能力识别谁在和它说话。所以一个好的软件黑客会让你把它放在电话旁边的会议桌上，它可以让电话会议上的每个人都知道是谁在说话。

### 我错过了太多！

展出的东西太多了。很遗憾我没有更多的时间去看所有的东西，但是我也想和所有这些了不起的人一起聊天。总是有一个黑客在进行中，因为你不想错过这样一个参加黑客大会的机会！