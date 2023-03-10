# Arduino 带… PIC？

> 原文：<https://hackaday.com/2016/11/13/arduino-with-a-pic/>

在 Arduino 占领业余爱好市场(嗯，至少是 8 位市场)之前，大多数黑客都使用 PIC 处理器。它们价格便宜，易于编程，具有良好的工具链，并且是基本印记的核心，是许多微控制器开发人员的入门药物。

[AXR·阿姆鲁]一直在与 Pinguino 合作，这是一款基于 PIC(当然，是 18F PIC，尽管你也可以使用 32 位设备)的 Arduino 处理器。他向您展示了如何用大约 12 个器件在试验板上构建兼容电路。PIC 有内置 USB。一旦你刷新了正确的引导程序，你就不需要任何东西，只需要一根 USB 线就可以编程了。你可以在下面看到一个视频。

你需要一个程序员来获得初始引导程序，但是有很多便宜的选择。IDE 可用于 Windows、Linux 和 Mac。当然，你可能想知道为什么你会使用 PIC 设备而不是更传统的 Arduino 设备。答案是:看情况。从功耗到 I/O 设备，再到可用性和价格，每个芯片都有自己的优缺点。这些芯片可能适合你，也可能不适合。这是你的电话。当然，[微芯片和 Atmel](https://hackaday.com/2016/10/18/whats-the-deal-with-atmel-and-microchip/) 之间的差异最近也变小了。

我们之前已经用专用板覆盖了 Pinguino。如果你从未玩过一枚[基础邮票](https://hackaday.com/2015/08/27/before-arduino-there-was-basic-stamp-a-classic-teardown/)，你可能会喜欢了解更多。如果你正在寻找 PIC 18F 无法处理的更大功率，你可以考虑 [Fubarino](http://fubarino.org/) ，一种可以与 Arduino IDE 一起使用的 PIC32 板。

 [https://www.youtube.com/embed/w_AkL6D9U7U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/w_AkL6D9U7U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

