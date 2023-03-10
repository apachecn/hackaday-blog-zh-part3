# Hackaday 奖参赛作品:为小型显示器添加 HDMI

> 原文：<https://hackaday.com/2016/05/27/hackaday-prize-entry-adding-hdmi-to-small-displays/>

液晶显示器有很多种尺寸，有很多关于将像素数据推送到更大显示器的文章。较小的液晶显示器，如 4、5 和 7 英寸的那种，用得不多，因为似乎没有人知道如何驱动这些东西。在[Joe]的 Hackaday Prize 参赛作品中，[他正在为微型液晶显示器](https://hackaday.io/project/11447-oli-open-lcd-interface)创建一个开源接口，使得为所有带有 HDMI 端口的设备添加一个接口变得简单而廉价。

[Joe]的开放式 LCD 接口有两块板，第一块板提供与 LCD 的连接，所有需要的电源电路，以及一堆用于断开每条 IO 线的焊盘。拼图的第二部分是一个解码器，它接收 HDMI 信号并驱动一个小 LCD。

HDMI 解码器对于爱好电子产品的世界来说并不新鲜——有多个项目[通过 HDMI](http://www.harbaum.org/till/dvi2par/index.shtml) 为 BeagleBoard 提供显示。甚至 Adafruit [也出售这种转换器](https://www.adafruit.com/products/2219)。[Joe]的主板还有另一个锦囊妙计:它也能给任何微控制器提供高分辨率显示。

还有另一个模块连接到[Joe]的分线板，将 LCD 变成 SPI 显示器。这意味着任何微控制器都可以驱动高分辨率显示器。它也很快:在下面的视频中，[Joe]的 SPI 显示器至少可以像我们见过的任何其他基于微控制器的显示器一样快地推动像素。

这是一个伟大的项目，通过打开易贝和阿里巴巴上百万廉价液晶显示器的大门，[乔]手中有一个获得 Hackaday 奖的好机会。

 [https://www.youtube.com/embed/f5_doUb3G6o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/f5_doUb3G6o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2016](http://hackaday.io/prize) is Sponsored by: [![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](http://hackaday.io/atmel)  [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](http://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](http://www.digikey.com/)  [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](http://supplyframe.com/)