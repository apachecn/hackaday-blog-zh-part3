# 逆向工程假人指南

> 原文：<https://hackaday.com/2017/02/13/dummies-guide-to-reverse-engineering/>

[Juan Carlos Jiménez]已经对一个路由器进行了逆向工程，具体来说，是一个华为 HG533。虽然这本身听起来可能不太重要，但他所做的是写了一系列博客帖子，这些帖子可以作为任何想要开始嗅探硬件的人的伟大教程。在这个由五部分组成的系列文章中，他详细介绍了如何识别打开固件之门的硬件串行端口，并查看了其中发生的事情。

第一部分处理在硬件上找到一个或几个调试端口，并识别三个重要的引脚-Rx、Tx 和 GND。这时，他向新手展示了他的第一个技巧——用手电筒从 PCB 下方照射，寻找有走线连接的引脚(最有可能是 Rx 和 Tx)、没有任何连接的引脚(最有可能是 CT 和 DTR)以及有连接到铜浇注层的引脚(最有可能是 VCC 和 GND)。当器件上电时，Tx 信号将被上拉并传输数据，而 Rx 信号将悬空，从而易于识别。不过，要找到波特率，要么需要一个逻辑分析器，要么就得玩一点猜谜游戏。

一旦你访问了串口并知道了它的波特率，就可以把它连接到你的电脑上，并使用几种方法中的任何一种来查看从那里传来的东西，例如 minicom、PuTTY 或 TeraTerm。有了对设备 CLI 的访问，以及在需要时找到登录凭证的运气，事情开始变得有趣起来。

在接下来的部分中，他将讨论如何跟踪数据路径，在本例中，他将着眼于主处理器与闪存之间的 SPI 信号，并解释如何有效地使用逻辑分析仪并对其捕获的信息进行解码。进一步，他展示了如何连接 USB 到 SPI 桥，将其连接到闪存，进行固件的内存转储并读取提取的数据。他深入固件，试图收集一些有用的信息，从而完成了这项工作。

这是一个很棒的系列，他对这个特定的硬件进行了详细的分析，并提供了许多通用的技巧，对于那些在开始调试硬件时需要一些帮助的人来说，这是一个完美的起点。

感谢[gnif]发布这个技巧。

 [https://www.youtube.com/embed/OJOCm0IIbPE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/OJOCm0IIbPE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

