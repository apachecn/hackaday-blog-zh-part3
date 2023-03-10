# Hackaday 奖参赛作品:一个数控等离子台

> 原文：<https://hackaday.com/2016/08/20/hackaday-prize-entry-a-cnc-plasma-table/>

数控路由器和 3D 打印机很酷，但据我所知，汽车和重型机械并不是由木材和塑料制成的。如果你想要一台可以制造其他机器的机器，你需要一台数控等离子切割机。那是[威尔巴登]参加黑客日奖的作品。它很大，很重，而且已经开始切割了。

一台等离子数控机床和一台简单的数控路由器没有太大的区别。[will]的桌面控制器只是一个附着在 Arduino 上的 GRBL 防护罩，轴承是从许多复印机上偷来的，你的电机和驱动器相当标准，除非它们对于一个简单的 3D 打印机来说过于庞大。

[威尔]真正的锦囊妙计是控制器接口。为此，他安装了一个树莓派显示屏，一个大而闪亮的红色按钮，以及漂亮的生锈焊接外壳后面的所有相关电子设备。构建的这一部分只是将 gcode 发送到 GRBL 屏蔽，而且是可靠地发送。现在[will]正在寻找一些方法来保存、安排和排列 Pi 上的工作，这个问题几乎——但不完全——与 Octoprint 做的工作相同。一个为大的、普通的、喷射奇异物质状态的 CNCs 开发的软件是一个有趣的项目，我们迫不及待地想知道这个项目将走向何方。

The [HackadayPrize2016](https://hackaday.io/prize) is Sponsored by:[![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](https://hackaday.io/atmel) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://www.digikey.com/) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/)