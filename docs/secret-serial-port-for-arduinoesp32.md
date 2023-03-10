# Arduino/ESP32 的秘密串行端口

> 原文：<https://hackaday.com/2017/08/17/secret-serial-port-for-arduinoesp32/>

如果您使用 Arduino IDE 对 ESP32 进行编程，您可能会对[Andreas Spiess'] [最新视频](https://www.youtube.com/watch?v=GwShqW39jlE)(见下文)感兴趣。在这篇文章中，他展示了一个在 Arduino 程序中使用所有三个 ESP32 UARTs 的例子。他称第三个端口为“秘密”，尽管这实际上是一个误称。然而，它确实需要对 Arduino 库进行快速修补才能工作。

获得额外的 UARTs 并不难。您只需使用一个可用的附加串行端口对象。然而，使能 UART 1 会导致 ESP32 崩溃！原因是默认情况下，UART 1 使用与 ESP32 闪存相同的引脚。

幸运的是，该芯片有一个矩阵开关，可以将几乎任何逻辑 I/O 引脚放在任何物理 I/O 引脚上。[Andreas]展示了如何修改代码，使 UART 1 映射到未使用的引脚，从而使一切正常工作。这是一个简单的变化，将两个参数替换为一个调用，该调用映射 I/O 引脚。如果您愿意，可以使用该技术将 UARTs 迁移到其他地方。

如果你想了解更多关于 ESP32 的信息，我们为你准备了一套很好的教程。或者如果你只是想快速浏览一下，你可以从这里开始。

 [https://www.youtube.com/embed/GwShqW39jlE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/GwShqW39jlE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

