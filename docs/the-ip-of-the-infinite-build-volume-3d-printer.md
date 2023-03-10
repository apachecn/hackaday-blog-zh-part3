# 无限构建体积 3D 打印机的 IP

> 原文：<https://hackaday.com/2017/06/06/the-ip-of-the-infinite-build-volume-3d-printer/>

上周，Blackbelt 3D 打印机[在 Kickstarter](https://www.kickstarter.com/projects/814534542/blackbelt-3d-printer) 上发布。Blackbelt 3D 打印机与 Kickstarter 上的任何其他 3D 打印机有何不同？这台打印机具有无限的制造容量。它是为连续生产而设计的。只要你有一个足够大的灯丝卷轴，这台打印机就会不间断地生产塑料部件。黑带是一台真正非凡的创新机器。是的，它有点贵，但它是为生产和制造而设计的，而不是某个家伙在他的车库里修修补补。

然而，[black belt 3D 网站](http://blackbelt-3d.com/)中的两个词让 3D 打印机界一片哗然。鉴于该行业的历史和 2010 年 3D 打印机大觉醒期间先行者的一些糟糕决定，社区中没有人希望看到“专利申请中”。允许连续生产的无限构建容量打印机的想法并不新鲜；[我们去年三月在中西部说唱节上看到过一个。因此，问题是即将到来的 Blackbelt 专利涵盖什么，现有技术是什么，以及是否仍然有可能建立一个使用这些创新技术的开源打印机？](http://hackaday.com/2017/03/25/mrrf-17-the-infinite-build-volume-printer/)

[![](img/2276e8ce111fe5bac4c441247245a160.png)](https://hackaday.com/wp-content/uploads/2016/04/abp.jpg)

MakerBot’s Automated Build Plate. Once available as Open Source Hardware, the Automated Build Plate has been expunged from MakerBot literature, patented, and apparently forgotten. [[Makerbot](https://commons.wikimedia.org/wiki/File:Automated_Build_Platform_for_Thing-O-Matic.jpg) CC-BY]

### 自动化构建平台的经验

关于 Blackbelt 打印机的问题在上个月试运行后不久就出现了。简单地说，这是几个月内展示的第二台打印机，它使用倾斜的打印平面和传送带，允许在无限的生产量中连续生产。

这种设计的首次公开实施[是在 2016 年的 Rapid 和 3 月份的中西部 RepRap Festival](http://hackaday.com/2017/03/25/mrrf-17-the-infinite-build-volume-printer/) 上，这是【Bill Steele】的产品。[Steele]没有发布*的产品*，这只是一个想法的高潮，这个想法始于 MakerBot 和他们的[自动化构建平台](http://www.thingiverse.com/thing:4056) (ABP)的机电一体化中指。

ABP 在发布时非常聪明，在 MakerBot 全盛时期，它被用于生产，为 Thing-O-Matic 制造零件。不幸的是，APB 被 MakerBot 申请了专利，所有对 ABP 的引用都被从 MakerBot 网站上删除了，所有基于开源传送带的生产机器的开发都停止了。

简而言之，3D 打印机社区以前见过类似的东西。首先，社区创造了一个创新的设备，使打印机更好，然后颁发专利。不管持有专利的公司是否成功，这种设备的公开开发就此停止，我们要等上几十年，直到专利到期。这种事以前发生过，以后还会发生。

### 现有技术对现有技术

[Bill Steele]在 2016 年 Rapid 和 2017 年 3 月的中西部 RepRap 节上首次展示了他未命名的 infinite build volume 打印机。然而，大家都不知道的是，Autodesk 的 Andreas Bastian 多年来一直在研究一种类似的设备。[Lum 打印机](http://www.andreasbastian.com/Lum-Printer)实际上与【Steele】演示的是同一台机器；倾斜的 XY 挤压平面上方的传送带底座允许打印无限长的内容。[有这台打印机工作的视频](https://www.youtube.com/watch?v=8HeHvglVJcs)，虽然 Lum 打印机从未被充分利用——大多数演示都是很长的单层面板——但它实际上是同一台打印机。

### 黑带专利

Blackbelt 3D 仍在申请专利，我们不知道这些专利声称什么。然而，Blackbelt 很友好地分享说，他们只是声称，“皮带材料，挤压平面的可调角度，和 g 代码操作。”对于 infinite build volume 打印机的开源实现者来说，其他一切都是公平的。

### 对 RepRap 社区的公开挑战

虽然 Blackbelt 的专利将涵盖*可变*倾斜床、皮带材料和转换 g 代码的方法，因此任何切片机都可以使用这种打印机，但这并不意味着开源无限量打印机的想法是不可能的。任何人需要做的唯一一件事就是用一个许可的许可证简单地构建一个。

[![](img/a7a1f002dadb33bd8c75a820a59d85f8.png)](https://hackaday.com/wp-content/uploads/2017/06/tilted-conveyor-3d-printor-bed-wb.jpg)

The product of a G-code shifter. From [wjsteele](https://www.thingiverse.com/thing:2358314).

这是对整个 3D 打印社区的挑战。想出一个打印机设计，使用与打印平面倾斜 45 度的底座，并找到合适的皮带材料。回报将是巨大的。为了让你开始，[比尔斯蒂尔]的 MRRF 建立使用 Kapton 和纸。我对此做了一些研究，我怀疑皮带材料可能有一个非常奇怪的来源:每个假日快捷酒店的煎饼机器人都使用一种特氟隆涂层的硅胶皮带，大小刚好适合 3D 打印机。这些薄饼机器人的制造商将皮带作为替换零件出售。

除了皮带材料，制造倾斜床 3D 打印机唯一需要的另一项技术是 g 代码机械手。对于这种类型的打印机，不需要不同的切片方法；Blackbelt 专利将描述一种操纵原始 g 代码的“曲速引擎”。幸运的是，[斯蒂尔]上传了他自己的 g 代码移位器。倾斜床打印机的 g 代码问题已经解决，并且是开源的。

真的，开源 3D 打印机唯一需要的就是床料和设计。当然，购买一卷超过 5 公斤的长丝也是一个问题，但如果这是最大的问题，我们都在一个伟大的地方。