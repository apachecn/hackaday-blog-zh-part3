# Hackaday 奖参赛作品:线性 CCD 突破

> 原文：<https://hackaday.com/2016/07/31/hackaday-prize-entry-a-linear-ccd-breakout/>

线性 CCD 是一个非常酷的组件。它们可以用于 DIY 光谱仪，如果你非常喜欢冒险，那就是 90 年代早期那些蹩脚的手持扫描仪的自制版本。不过，在这些部件周围，线性 CCD 看不到太多用途，这使得[esben]的 Hackaday 奖参赛作品非常酷。[他正在打造一个突破，让这些线性 CCD 的使用更容易](https://hackaday.io/project/9829-linear-ccd-module)。

线性 CCD 模块看起来像一个过度生长的 DIP 芯片，在几千个像素的正上方有一个玻璃窗口，呈直线排列。来自这些像素的数据并不是以一系列 1 和 0 的形式输出的:这是一种传统，CCD 产生的数据是模拟的。这意味着从这些模块中的一个读取光需要具有良好 ADC 的快速微控制器。

对于这个项目，[esben]使用的是 Nucleo F401RE，这是一种围绕 STM32F4 微控制器构建的开发板。该处理器速度足够快，可以从其 12 位 ADC 读取数据，并存储所有三千个像素。现在的问题是如何将这些数据从微控制器中取出并放到存储器中。在 UART 限制为 230kB/s 的情况下，[CCD 的每个“帧”需要 300ms 才能传输到计算机](https://hackaday.io/project/9829/log/41390-first-steps-with-uart)。[埃斯本]真的希望能做得更快一点，所以他正试图[黑掉 DMA 控制器来完成他的命令](https://hackaday.io/project/9829/log/41426-a-second-look-at-dma-plus-a-firmware-update)。看起来[esben]正在为一个非常普通的线性 CCD 制作一个快速接口，这意味着为我们所有人提供更多酷的工具和玩具。

The [HackadayPrize2016](https://hackaday.io/prize) is Sponsored by:[![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](https://hackaday.io/atmel) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://www.digikey.com/) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/)