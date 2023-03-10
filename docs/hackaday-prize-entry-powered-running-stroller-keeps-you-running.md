# Hackaday 奖参赛作品:电动跑步童车让你保持跑步

> 原文：<https://hackaday.com/2017/08/07/hackaday-prize-entry-powered-running-stroller-keeps-you-running/>

有一种叫做“跑步婴儿车”的婴儿车，可以带着你的孩子一起跑步，但如果你带着两个四岁大、38 磅重的孩子，顶着风，爬上足够多的山坡，你会很快失去动力。[Andrew Clink]的和他妻子的解决方案？将婴儿车改装成[自驱动的走鹃](https://hackaday.io/project/21470-roadrunner-powered-running-stroller)。

【Andrew】的 [hackaday.io 构建日志](https://hackaday.io/project/21470/logs)很详细，包括设计、计算、原理图、3D 打印文件、失败和重试等等。电力由一组驱动无刷电机的锂离子电池提供。该电机使用一个小电机滑轮和一个更大的 3D 打印滑轮周围的齿形带转动婴儿车的前轮，提供 13.92:1 的传动比。[Andrew]考虑了多种转向方法，甚至尝试了几种，但考虑到他的路径大部分是直线，只需要用手进行小的调整。为了防止婴儿车因为任何原因离开他，[Andrew]为他的手机编写了一个 iOS 应用程序，该应用程序利用了蓝牙 LE[邻近模式](https://www.bluetooth.org/DocMan/handlers/DownloadDoc.ashx?doc_id=303199&_ga=2.130979401.795644905.1501947231-1426662339.1501947231)。它使用一个 [nRF8001](https://www.nordicsemi.com/eng/Products/Bluetooth-low-energy/nRF8001) 蓝牙连接 IC 与一个小型遥控器进行通信，为了增加安全性，它还有一个皮带夹和一个停止按钮。

有用吗？自己看下面的视频。我们确信(安德鲁)和他的妻子在未来很长一段时间内将会继续保持健康。

[https://player.vimeo.com/video/226684620](https://player.vimeo.com/video/226684620)

也许你不是一个跑步者，更喜欢自己骑婴儿车？在这种情况下，你可以像[柯林·福尔泽]做的那样，制造一辆时速超过 53 英里的婴儿车。或者也许真的是让你的[宝宝自己骑](http://hackaday.com/2017/01/12/babys-first-hands-free-stroller/)，当然有防撞功能。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)