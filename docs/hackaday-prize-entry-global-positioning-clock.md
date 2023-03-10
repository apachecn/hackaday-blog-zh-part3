# Hackaday 奖参赛作品:全球定位时钟

> 原文：<https://hackaday.com/2017/10/27/hackaday-prize-entry-global-positioning-clock/>

你如何吸引成千上万 Hackaday 读者的注意？造一个钟！有太多的选择让你苦恼。你是用一个晶体作为时钟源，一个奇特的烤箱控制的晶体振荡器，还是仅仅是电源电压？你应该考虑在时钟里放一个 GPS 模块吗？所有这些都是非常有趣的问题，鼓励讨论或学习，这就是 Hackaday 的全部内容。时钟很酷，背后的工程更酷。

作为[Nick]的 Hackaday 获奖作品之一，[他正在建造一个极简的 GPS 时钟](https://hackaday.io/project/18501-gps-clock)。首先，每一个钟的核心，显示器。有八个七段显示屏，两个分别显示小时、分钟和秒，一个较小的数字显示十分之一秒。这些显示器由 ATXmega32E5 控制，这是该项目的早期版本的升级，仅使用 ATtiny 和 MAX6951 LED 驱动器。

GPS 魔法是这个项目变得非常酷的地方。[Nick]使用的是 sky traq venus 838 lpx-T(Tindie 上的分线板[也有提供)。该 GPS 芯片有一个方便的边缘安装 SMA 连接器来接收来自 GPS 卫星的信号，并有一个双向 UART 来转储 NMEA 时间码和 PPS 输出。通过结合时间码、PPS 输出和微控制器上的定时器，[Nick]拥有一个非常精确的时钟，看起来也很棒。](https://www.tindie.com/products/nsayer/skytraq-venus838lpx-t-timing-gps-module-breakout/)

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)