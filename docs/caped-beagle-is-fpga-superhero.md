# 披着斗篷的小猎犬是 FPGA 超级英雄

> 原文：<https://hackaday.com/2018/03/03/caped-beagle-is-fpga-superhero/>

我们怀念所有东西都有子板的日子。现在，Arduinos 有盾牌，Raspberry Pis 有帽子。比格骨有毛。随便啦。然而，不管名称如何，开源的[beagle wire](https://www.crowdsupply.com/qwerty-embedded-design/beaglewire)cape/shield/hat/daughter board 连接到一个 BeagleBone，并提供了一个 Lattice iCE40HX FPGA、一些支持硬件和常见的 I/O 连接器，如 Pmod 和 Grove。你可以在下面看到一个关于板子的视频。

除 FPGA 之外，该板还包含 EEPROM、RAM、flash 存储器、振荡器以及一些按钮、开关和 led。按钮甚至具有硬件去抖功能。零件清单和设计文件都是可用的，而且——取决于一次成功的众筹活动——你可能在未来花 75 美元就能买到一个。

该板配置为通过 100 MHz 16 位 GPMC 端口进行通信。Linux 软件和示例驱动程序是可用的，因此为了您自己的目的让 FPGA 和 CPU 相互通信应该是相当简单的。

如果您决定自己动手制作，只需点击一下按钮，就可以为您在 DigiKey 购物车中安装大部分组件。尽管 DigiKey 网站抱怨了一个错误，但它似乎订购了 26 个组件中的 24 个，总额刚刚超过 50 美元。当然，你仍然需要找到丢失的零件和电路板。

我们在过去已经谈了很多关于[格子冰 FPGA](https://hackaday.com/2015/08/19/learning-verilog-on-a-25-fpga-part-i/)的内容。你不仅有我们的教学视频，还有[很多其他的](https://hackaday.com/2017/10/24/fpga-design-with-free-software/)。

[https://player.vimeo.com/video/255801721](https://player.vimeo.com/video/255801721)

感谢[德鲁·富斯蒂尼]向我们指出这一点。