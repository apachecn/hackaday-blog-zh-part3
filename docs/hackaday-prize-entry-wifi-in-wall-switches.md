# Hackaday 奖参赛作品:墙壁开关中的 WiFi

> 原文：<https://hackaday.com/2017/04/07/hackaday-prize-entry-wifi-in-wall-switches/>

物联网和家庭自动化是下一件大事，尽管我们已经有了 40 年的 X10 开关和控制器。为什么突然对家庭自动化感兴趣？显然是带 WiFi、ZigBee 和 Z-wave 的廉价微控制器。对于这个 Hackaday 奖的参赛作品，【Knudt】[正在建造一个 WiFi 开关](https://hackaday.io/project/20035-modular-wifi-switch)，这意味着可以改装到任何欧洲墙壁开关中。

【Knudt】的 WiFi 墙壁开关有三个部分，每个部分都有不同的要求。顶层是开关本身和一个小有机发光二极管显示器。这些开关实际上是两个小电容开关，这意味着没有理由去寻找合适的机械开关。想法不错。这个装置的第二层基本上是一个 ESP8266，为这个墙壁开关提供所有的逻辑。底层更有趣一些，容纳 110-230V 输入，带有三端双向可控硅开关或继电器。这是有趣的，燃烧的事情发生的地方。

现在，你可以去当地的家居用品店，简单地*买*一个这样的设备。历史表明这是一个糟糕的想法。随着家庭自动化云服务的关闭和安全漏洞比比皆是，DIY 或开源家庭自动化项目确实是最好的主意。这使得[Knudt]的项目成为 Hackaday 奖的一个很好的参赛项目。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)