# PIC32 DMA SPI

> 原文：<https://hackaday.com/2016/09/26/pic32-dma-spi/>

[Mike]想要从 PIC32 驱动几个 SPI 外设。他展示了他的传统中断处理程序从他的主任务中带走了多少延迟。他需要更有效的方法。因此，他使用 DMA 创建了 [SPI 通道。他还制作了一个视频(见下文),非常清楚地解释了他为什么要这么做，并展示了关于这一切如何工作的示波器痕迹。](https://www.youtube.com/watch?v=XlKilhcP_ic)

虽然这个项目是针对 PIC32 的，但是关于 DMA 的讨论适用于任何具有直接存储器访问的计算机。唯一缺少的是代码。然而，你可以在网上看到大量的[例子](https://tahmidmc.blogspot.com/2014/05/simple-pic32-dma-example.html)，包括一个[微芯片网络研讨会](http://www.microchip.com/stellent/groups/SiteComm_sg/documents/DeviceDoc/en542870.pdf)。

DMA 是一种强大的技术，尽管调试起来有些棘手。大型计算机使用它来实现高性能 I/O 已经有很长时间了，比如磁盘驱动器或显示器。我们之前已经讨论过臂的 [DMA。毫不奇怪，驱动 led 似乎是 DMA](https://hackaday.com/2015/01/05/rgb-led-matrices-with-the-stm32-and-dma/) 的[常见用例。](https://hackaday.com/2014/12/04/microdma-and-leds/)

 [https://www.youtube.com/embed/XlKilhcP_ic?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XlKilhcP_ic?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

