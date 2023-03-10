# Hackaday 奖参赛作品:一本 E-Ink 日历

> 原文：<https://hackaday.com/2017/09/01/hackaday-prize-entry-an-e-ink-calendar/>

电子墨水显示器在 DIY 电子领域几乎变得很常见，现在我们有了非常强大的低功耗微控制器，其中一些具有某种无线连接功能。将这两者结合起来，你就有可能成为一个基本的信息屏幕——一个总是显示某种相关信息的低功耗设备，无论是日期还是天气。

为了他们的 Hackaday 奖参赛作品，和董正在制作一个电子墨水日历。这是一个日历，它显示位图，它可以显示时间，只要稍加修改，它就可以显示天气、当前交通状况或火车时刻表。如果这是 90 年代，我们会称之为信息设备，它会让所有人大吃一惊。

这种电子墨水日历的当前设计使用 800 x 600 像素显示器，以 16 级灰度模式工作。处理器是 STM32F4，在降低成本的版本中，外部 SRAM 被丢弃，帧缓冲区被移到内部 RAM。电子墨水显示器实际上非常快，允许在 1 位模式下超过 10 FPS。

与任何电子墨水项目一样，[驱动显示器是一个小噩梦](https://hackaday.io/project/11537-nekocal-an-e-ink-calendar/log/50303-a-description-about-the-epd-driving-method-used-in-this-project)，但是【文婷】能够以每秒几帧的速度驱动显示器。对于一个实际上不应该改变太多的设备来说，这已经足够好了——毕竟这是一个日历。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)