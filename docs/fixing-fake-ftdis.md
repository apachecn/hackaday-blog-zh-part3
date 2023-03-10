# 修复假 FTDIs

> 原文：<https://hackaday.com/2017/03/07/fixing-fake-ftdis/>

如果你知道在互联网上去哪里，你可以拿起一个 1.67 美元的 FTDI USB 到串行适配器，全球免费送货。这个板上的芯片是 FTDI FT232RL，数量上大约花费两美元。这意味着廉价适配器上的芯片是假冒的。虽然你可以用合法的芯片购买 USB 转串行适配器，但[Syonyk]找到了一个更便宜的解决方案:购买假冒的适配器，一些正版芯片，[并重新加工 PCB](https://syonyk.blogspot.com/2017/03/fixing-fake-ftdi-ft232rl-adapters-ssop.html) 。这是辉煌的，一个脱焊能力的出色展示。

为什么[Syonyk]要用真正的 FTDI 替换非正版芯片？[最好的原因是 FTDIgate Mk. 1](http://hackaday.com/2014/10/22/watch-that-windows-update-ftdi-drivers-are-killing-fake-chips/) ，Windows 官方 FTDI 驱动检测到非正版芯片，将 USB PID 设置为零。这阻塞了一大堆设备，通常被认为是一个糟糕的举动。 [FTDIgate Mk. 2](http://hackaday.com/2016/02/01/ftdi-drivers-break-fake-chips-again/) 是一个主题的变体，如果发现非正品零件，FTDI 驱动程序会将垃圾数据注入电路。这也可能是砖块设备。尽管存在驱动问题，但用真芯片替换假芯片的最佳理由是更高比特率的性能；[Syonyk]以 3 Mbps 的速度工作，而假芯片没有那么快。

为了更换伪造的芯片，[Syonyk]在引脚上覆盖了一大团焊料，仔细加热芯片的两面，当所有东西都熔化时，将有问题的芯片滑下。一点焊接编织，电路板准备好了真正的芯片。

有了新的芯片，廉价的 USB 到串行适配器板可以完美地工作，尽管任何试图重复这些工作的人可能都希望用 USB 微型端口取代 USB 微型端口。