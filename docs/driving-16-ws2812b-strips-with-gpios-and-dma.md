# 利用 GPIOs 和 DMA 驱动 16 个 WS2812B 条带

> 原文：<https://hackaday.com/2016/10/06/driving-16-ws2812b-strips-with-gpios-and-dma/>

[Martin Hubáek]与[一起为 STM32F3 系列处理器编写了他的 WS2812 LED 库](https://github.com/hubmartin/ws2812b_stm32F3)。[马丁]的图书馆采取了和[保罗·斯托弗雷根]的[10 月 28 日](https://github.com/PaulStoffregen/OctoWS2811)给青少年的，和[埃里克·斯蒂格]的[给飞思卡尔 FRDM-K64F 董事会](https://mcuoneclipse.com/2015/08/05/tutorial-adafruit-ws2812b-neopixels-with-the-freescale-frdm-k64f-board-part-5-dma/)的同样的方法。也就是说，它使用三个 DMA 通道来尽可能快地将信号输出。

[![ws2812b-dma-timing-diagram](img/c28a5e3794a3a36958f5611f9f8bd821.png)](https://hackaday.com/wp-content/uploads/2016/10/ws2812b-dma-timing-diagram.png) 他有一个很好的[方法概述](http://www.martinhubacek.cz/arm/improved-stm32-ws2812b-library)你可以查看一下细节，不过是这样的。WS2812 使用类似 PWM 的编码来传输数据。如果信号在 1/3 的时间内为高，则为 0，如果信号在 2/3 的时间内为高，则为 1。

第一个 DMA 信号发送一个位的起始，将所有输出设为高电平。第二个 DMA 通道发送所有 0 的低电平信号，第三个 DMA 通道发送 1 的低电平信号。这三个 DMA 中的每一个都以正确的时间计时，以使脉冲定时工作。

与其他方法相比，这种 GPIO/DMA 设置的优势在于，它可以驱动一整排引脚，对于 STM32F10x 芯片，最多可同时驱动 16 条引脚。它还循环图形缓冲区，这样您就可以在不使用太多内存的情况下驱动重复的模式。CPU 所要做的就是在 DMA 缓冲区(一半)空的时候加载它，这意味着即使 led 满载，它仍有大部分时间用于处理数字。

[![ws2812b-mixing-colors-with-and_or-gates-urwhqbio1qemkv-shot0006_white](img/51b86edb9423ae94015c14e6c1faa254.png)](https://hackaday.com/wp-content/uploads/2016/10/ws2812b-mixing-colors-with-and_or-gates-urwhqbio1qemkv-shot0006_white1.jpg) 最后，为了炫耀，【马丁】使出了一个甜蜜的花招，并用视频捕捉了下来。由于数字信号是针对红色、绿色和蓝色通道进行开/关编码的，他决定尝试数字混色。他将两个同时发生的信号放在一起，并演示了它的工作方式，正如你所期望的那样。看看下面的视频吧。

 [https://www.youtube.com/embed/UrwhQBIo1qE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/UrwhQBIo1qE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

