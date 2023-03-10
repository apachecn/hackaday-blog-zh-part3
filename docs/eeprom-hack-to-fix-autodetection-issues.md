# EEPROM 黑客修复自动检测问题

> 原文：<https://hackaday.com/2017/01/29/eeprom-hack-to-fix-autodetection-issues/>

硬件的自动检测是让普通用户更容易使用计算机的主要部分。Amiga 在其 Zorro 总线上有自动配置，微软开发了即插即用，苹果使用了由麻省理工学院开发的 NuBus。在现代，这是我们已经习以为常的事情，但它并不总是正确的。[Evan]遇到了这个问题，[一个在 Linux](https://abzman2k.wordpress.com/2015/09/22/pv981a-16-mod-for-autodetection-in-linux/) 下不能正确自动检测的视频采集卡。

视频捕捉卡由四个 PCI 捕捉卡组成，每个卡有四个输入，通过 PCI 到 PCI-E 总线芯片连接，总共十六个输入。找到问题的原因并不太困难——驱动程序检测到该卡是一个具有 8 个输入的不同型号，而不是卡上实际存在的 16 个输入。驱动程序通过卡报告的唯一标识符来检测插入的设备。卡上的代码与具有不同硬件的不同型号的卡上的代码相同，导致了问题。

作为一个快速测试，[Evan]试图篡改驱动程序选择，强制使用一个 16 输入模型的驱动程序。这是成功的——所有 16 个输入都可以使用了。但这不是一个可移植的解决方案，而且每次卡需要重新安装或移动到不同的计算机上时，[Evan]都必须记住这个黑客。

进一步观察硬件，[Evan]发现该卡上有四个 24c02 EEPROM 芯片，每个 PCI 卡一个。通过转储内容，他们识别出了驱动程序用来确定卡的型号的唯一标识符。然后，将该值更改为与 16 输入卡相对应的值是一项简单的工作，通过将新值烧录到 EEPROM 来实现功能自动检测。[Evan]然后[在 LinuxTVWiki 页面](https://abzman2k.wordpress.com/2015/09/22/pv981a-16-mod-for-autodetection-in-linux/)上发布了这些发现。

这是一个整洁的黑客技术，也是一个非常具有前瞻性的技术——十年后，如果这张卡被扔进了另一张卡的垃圾箱，他们将很容易就能让它运行起来。了解自动检测的来龙去脉将会对你的黑客生涯有所帮助。在 USB 中，它是通过 PID 和 VIDs 来完成的，关于这些是如何分发的，还存在一些争议。