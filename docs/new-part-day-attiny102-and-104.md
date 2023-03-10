# 新零件日:第 102 和 104 天

> 原文：<https://hackaday.com/2016/08/01/new-part-day-attiny102-and-104/>

Atmel 今年早些时候推出了一些新的小型微控制器芯片，我们现在才开始考虑如何使用它们。ATtiny102 和 ATtiny104 ( [数据表](http://www.atmel.cimg/Atmel-42505-8-bit-AVR-Microcontroller-ATtiny102-ATtiny104_Summary.pdf))售价约为 1 美元(US)，采用易于管理的 SOIC 封装，分别有 8 个和 14 个引脚。不过这是一种奇怪的芯片，其功能介于米粒大小的 ATtiny10 和 hacker-staple ATtiny25-45-85 系列之间。

ATtiny104 有一堆不贵的别针。它有一个真正的硬件 USART，这是其他低端 AVR 所没有的，它能够在主机模式下进行 SPI。它只有一个计数器，但它是一个 16 位计数器，并且它有完整的 AVR 10 位 ADC，而不是 ATtiny10 的有限 8 位 ADC。它与 ATtiny10 共有的最大限制是，它只有 1 KB 的程序闪存和 32 个*字节*(!)的内存。你可能会想用汇编语言给这个怪物编程。

请继续阅读更多评论，并在最后查看[kodera2t]的视频评论。

## 复习

[![attiny_comparison](img/b07a60d548ce47bb5a03305606270579.png)](https://hackaday.com/wp-content/uploads/2016/07/attiny_comparison.png)[第一篇评论](http://syncchannel.blogspot.de/2016/03/checking-out-new-atmel-attiny102104.html)来自【丹·沃森】的博客。他在 3 月份买了一个 Atmel Xplained 104 Nano 评估板，并对其进行了测试。我们不知道他当时是如何以低于 5 美元的价格得到一个，但这个工具包似乎可以从通常的嫌疑人那里以低于 10 美元的价格得到。

解释工具包很有趣。它有一个相对强大的 ATmega32u4 作为系统内编程器和 USB 串行连接器。这很有趣，因为编程器的成本是被测设备的两倍。

[Dan]还提供了一个不错的小型 AVR 器件对比图。(点击 embiggen。)

几个月来，[kodera2t]一直在将 ATtiny 系列芯片推向最大，所以我们很高兴看到他的[对 attini 102](https://hackaday.io/project/10116-minimalist-a-go-go/log/35605-very-brief-review-of-atmels-new-attiny-102)的评论。考虑到芯片名称(T102-ES)，他设法为自己弄到了一些工程样品，这是额外的亮点，但不应该让你气馁，因为零件现在已经在商店里了。

[![attiny102_104_pinouts](img/c679a43ced8008b9cd0b7e9e226403f4.png)](https://hackaday.com/wp-content/uploads/2016/07/attiny102_104_pinouts.png)【kodera 2t】不再与评估委员会合作，一切从零开始。也许这就是为什么他强调 ATtiny102 部件的*新引脚*。特别是，GND 引脚是其他 ATtiny 芯片(！idspnonenote)上 VCC 引脚所在的位置。).阅读数据手册是值得的。虽然我们脾气暴躁，讨厌变化，但新的引脚排列更加合理，VCC 和 GND 引脚一起位于芯片顶部，就在你想添加去耦电容的地方。

如果你习惯使用 ATtiny 部件，还有一个小问题。由于 ATtiny104 有 14 个引脚，因此 GPIOs 分为两个 8 位组:PORTA 和 PORTB。ATtiny102 似乎是 104 的精简版，这意味着尽管它只有 6 个 GPIO 引脚，但它们仍然分布在两个存储体中，每个存储体中有 3 个引脚。如果您习惯于一次将整个字节写入 GPIO 输出，这将迫使您改变编码习惯。

## 使用

[![brief-review-of-attiny102-2j4y0pxxnq0mkv-shot0005_thumbnail](img/96b2f85737f9228cefd0bc1116d1730f.png)](https://hackaday.com/wp-content/uploads/2016/07/brief-review-of-attiny102-2j4y0pxxnq0mkv-shot0005_thumbnail.png) 我们发现自己抓耳挠腮，问这个芯片到底有什么用。小型廉价封装的 USART 是一大特色。类似 ATtiny14 的东西，有 11 或 12 个免费的 GPIO 引脚，非常适合非常小的项目。但是我们不能完全理解 32 字节的 RAM。例如，无论 USART 有什么样的应用，都必须考虑短接收缓冲区，并在运行中进行处理。仅 c 启动代码就要花费几百个字节，在 RAM 如此有限的情况下，我们猜测汇编代码是唯一合理的选择。

当然，在设计和营销这款芯片时，黑客市场可能还不在 Atmel 的考虑范围之内。它一定有利于一些我们还不太清楚的工业用途。什么东西需要 USART 但不需要太多程序或 ram？你能想出这种小众设备的用途吗？

 [https://www.youtube.com/embed/2J4y0pxXNq0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2J4y0pxXNq0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

