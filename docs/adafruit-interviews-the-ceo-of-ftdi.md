# Adafruit 采访 FTDI 的首席执行官

> 原文：<https://hackaday.com/2016/02/08/adafruit-interviews-the-ceo-of-ftdi/>

说到电子爱好者和 EEs，没有哪家公司比 FTDI 更值得关注。他们以 USB 转换器芯片而闻名，即今天仍然非常流行的 USB 转串行芯片。事实上，这些芯片如此受欢迎，以至于在中国售价 2 美元的 Arduinos 和其他非常低成本的设备中经常可以找到这些芯片的克隆产品。一年多前，一些聪明人注意到 [FTDI 驱动程序通过将 USB PID 设置为 0000 来阻止这些假冒芯片](http://hackaday.com/2014/10/22/watch-that-windows-update-ftdi-drivers-are-killing-fake-chips/)。互联网对这一举动做出了反应， [FTDI 很快从这一立场上做出了让步。Windows 驱动被修复了大约一年](http://hackaday.com/2014/10/24/ftdi-screws-up-backs-down/)，直到同样的恶作剧再次被发现。

[Adafruit 最近采访了 FTDI](https://blog.adafruit.com/2016/02/08/exclusive-interview-with-fred-dart-ceo-of-ftdi-ftdichip-ftdi-adafruit/) 的首席执行官【Fred Dart】，向我们提供了并非来自对 Windows 自动更新驱动程序感到失望的人们的第一手事实和数据。[弗雷德·达特]提供的最有趣的信息是，FTDI 最初是如何发现这些假冒芯片的，哪些 FTDI 芯片正在被假冒，以及有多少不同的公司正在仿制这些芯片。

该公司第一次意识到他们正在被克隆，因为他们无法重现中国制造的“FTDI”USB 到 RS232 电缆的奇怪行为。电缆样本被运送到 FTDI，在检查了内部的芯片后，FTDI 发现这是一个克隆产品，其架构与真正的芯片明显不同。

到目前为止，伪造者似乎只是在伪造 FT232RL 的 SSOP 版本，偶尔也会伪造更老的 FT232BL 芯片。从 FTDI 看到的情况来看，似乎只有一两家公司在伪造芯片。

作为 FTDI 的首席执行官，[Fred]对于如何阻止中国的造假者有一些见解。最重要的是商标的标志。这不仅仅是一个网页的标志，而是一个可以被激光蚀刻到芯片塑料包装上的标志。美国海关一直非常愿意识别假冒组件，这导致了几批货物被销毁。然而，法律行动在中国有点困难，FTDI 正在对付一个不止伪造 FTDI 芯片的团伙；这个团伙很有可能在几年前制造了假冒的 PL23o3 芯片。

就 FTDI 打击假冒芯片而言，[Fred Dart]并没有在这个问题上保持沉默，他只是没有被问到这个问题，也没有自己提出来。