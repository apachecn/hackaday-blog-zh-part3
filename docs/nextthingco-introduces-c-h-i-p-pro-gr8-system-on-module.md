# NextThingCo 在模块上引入了 C.H.I.P. Pro、GR8 系统

> 原文：<https://hackaday.com/2016/10/12/nextthingco-introduces-c-h-i-p-pro-gr8-system-on-module/>

NextThingCo 是非常受欢迎的惠普单板 Linux 电脑的制造商，它发布了最新版本的硬件。这是 C.H.I.P. Pro ，一款 SBC，旨在成为你下一个伟大项目、产品或物联网的嵌入式大脑。

C.H.I.P. Pro 采用主频为 1 GHz 的 Allwinner R8 ARMv7 Cortex-A8、MALI-400 GPU 和 256 MB 或 512 MB NAND 闪存。Pro 还具有 802.11 b/g/n WiFi、蓝牙 4.2，并通过了 FCC 的全面认证。这款主板将于 12 月上市，预计售价 16 美元。

C.H.I.P. Pro 的设计融合了设计用于安装在产品中的模块和设计用于试验板的单板计算机。它像数百个其他模块一样具有堞形边缘，但这种设计意味着组装不会像扔一些浆糊和回流所有东西那么简单。C.H.I.P. Pro 的特点是两面都有器件，这使得回流很成问题，需要 0.1 英寸的接头或 PCB 上的切口。作为一台单板电脑，这个东西体积小，功能强大，是树莓派 Zero 的有力竞争对手。一个 C.H.I.P. Pro 开发套件包括两个 C.H.I.P. Pro 单元、一个“调试”板和用于试验板的接头，售价 49 美元，预计发货日期为 12 月。

一个 16 美元的带有 WiFi、蓝牙、没有 NDA 的 Linux 模块很不错，但也许更有趣的宣布是 NextThingCo 也将出售为 C.H.I.P. Pro 提供动力的模块。

GR8 模块包括一个运行在 1 GHz 的 Allwinner R8 ARMv7 Cortex-A8、一个 MALI-400 GPU 和 256 MB DDR 3 SDRAM。外设包括 TWI、两个 UARTS、SPI (SD 卡支持被黑客攻击到此)、两个 PWM 输出、一个 6 位 ADC、I2S 音频、S/PDIF、一个 USB 2.0 主机和一个 USB 2.0 OTG，以及一个并行相机接口。这不是一个真正的视频输出芯片，但它支持电视输出和并行 LCD 接口。GR8 的有限数据表可在 [NextThingCo GitHub](https://github.com/NextThingCo/CHIP_Pro-Hardware/blob/master/Datasheets/GR8_Datasheet_v1.0.pdf) 上获得。

将整个 Linux 系统放在单个 BGA 模块上必然会与最近发布的 Octavo Systems OSD355X 系列相提并论，该系列最广为人知的名字是芯片上的[beagle bone](http://hackaday.com/2016/05/10/new-part-day-a-beaglebone-on-a-chip/)。机械方面，Octavo 芯片更容易焊接。尽管它的球数几乎是 GR8 的两倍，Octavo 有 400 个球，GR8 有 252 个球，但 Octavo 的球间距要宽得多，这使得逃跑路线更容易。

比较 OSD355X 和 GR8 之间的外设，有点不公平，OSD 在以太网、更多 RAM 和花哨的 TI PRUs 方面略微领先。关于定价，GR8 在任何数量的芯片上的价格都是 6 美元。这大大低于 OSD355X。

最初的 C.H.I.P .在 NextThingCo 正在营销的社区中获得了非常好的反响，尽管该社区对 Allwinner CPUs、[令人生厌的 PR](http://www.prnewswire.com/news-releases/next-thing-co-admits-to-lying-about-9-computer-300184512.html) 和[关于 C.H.I.P.](http://www.cnx-software.com/2015/06/07/allwinner-r8-module-datasheet-and-price-is-the-9-c-h-i-p-computer-selling-at-a-loss/) 真实价格的问题很反感。C.H.I.P. Pro 肯定会有更多的用途，但 GR8 才是真正的故事。一个包含整个 Linux 系统的 jellybean 部件是一个疯子多年来狂热的梦想。GR8 使得将开放软件的力量投入到任何项目中变得更加容易，我们迫不及待地想看到它所允许的应用。