# 双 SDR 同时接收两个频段

> 原文：<https://hackaday.com/2018/05/21/dual-sdr-receives-two-bands-at-once/>

曾经有一段时间，软件定义无线电(SDR)的实验是一种舶来品。但是由于廉价的基于 USB 的硬件，这项技术现在任何人都可以使用。虽然玩 20 美元的小 u 盘很有趣，但你最终会想升级到更好的东西，而且有很多很好的选择。其中之一就是 SDRPlay，他们最近发布了一款新的硬件——RSP duo(T1)，它集成了双调谐器。

我们之前讨论过使用 SDRPlay 作为廉价加密狗的升级。新器件可以在 1 kHz 至 2 GHz 范围内调谐单个 10 MHz 频段，也可以选择两个 2 MHz 频段。这开启了许多需要拾取不同频谱区域信号的应用(例如，监控跨频段中继器的两端)。

你可能想知道如何利用这两个带软件的调谐器。有一篇网上评论报道了软件如何与双调谐器配合工作。您还可以从[seven 41 one]上看到一段展示收音机使用情况的视频。

除了双频带接收之外，像这样的单元还可以用于构建认知无线电、分集接收、降噪和无线电定位系统。您可以找到该器件的[规格表](https://www.sdrplay.com/wp-content/uploads/2018/05/RSPduoDatasheetV0.5.pdf)，其中显示它有一个 14 位转换器和几个天线、滤波器和参考时钟选项。

你可能会想，花将近 300 美元，你可以买一个以上的 USB 加密狗，并得到同样的结果。不过，使用 RSPduo 有很多好处。首先，具有扩展转换器和内置滤波器的 RSPduo 的性能会更好。它的频率范围也比廉价的加密狗宽。然而，对于任何想要了解两个信号之间关系的应用，使用多个 USB 设备将是棘手的，如果不是不可能的话。使用 RSPduo，数据在单个 USB 接口上，因此无需额外工作即可关联数据。

这并不是说不能使用多个 USB 设备，只是更难。RSPduo 与该公司早期的产品非常相似，只是增加了一个额外的调谐器。如果你想知道如何使用 RSPduo 的表弟，我们做了一个关于 SDRPlay 的 GNURadio 教程[。](https://hackaday.com/2015/11/12/your-first-gnu-radio-receiver-with-sdrplay/)

 [https://www.youtube.com/embed/8WNxtanfWIk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8WNxtanfWIk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

