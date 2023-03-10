# BeagleBone 绿色，现在无线

> 原文：<https://hackaday.com/2016/05/21/beaglebone-green-now-wireless/>

在过去的几年里，比格骨生态系统已经从最初的白色比格骨发展到两年后的黑色比格骨。黑色是 BeagleBone 家族的杀手锏，有一段时间在任何地方都买不到。TI 对 BeagleBone 中使用的 SoC 一直很友好，导致了去年发布的 beagle bone Green、专注于机器人技术的 T2 beagle bone Blue 以及最近发布的芯片上的 beagle bone。所有这些主板都具有相同的功能，针对不同的使用情况；芯片上的 BeagleBone 是一个单独的模块，可以放入 Eagle 原理图中。BeagleBone Green 是一款低成本的产品，与 Seeed Studio 的 Grove connectors 配合得很好。它们都是一个主题的变体，直到现在，无线还不是一个内置选项。

本周末在 Maker Faire 上，Seeed Studio 展示了他们最新版的 BeagleBone Green。这是 BeagleBone 绿色无线，包括 802.11 b/g/n 和蓝牙 4.1 LE。

由于所有的比格犬骨通常都是一样的，每个都有自己的特殊部分，所以对每个板进行逐行比较是公平的:

[![BeagleBones](img/64742571cb47e742e06d92dfbd4d5ab4.png)](https://hackaday.com/wp-content/uploads/2016/05/beaglebones.png)

虽然 BeagleBone Blue 仍在研发中，并将于今年夏天发布，但 BeagleBone Green Wireless 填补了 BeagleBone 生态系统中的 WiFi 和蓝牙利基市场。

### 无线的

[![Wireless](img/5e21e4ea8ef2885f4eeaf5e1e2afc6ff.png)](https://hackaday.com/wp-content/uploads/2016/05/wireless.jpg) 和任何一台运行 Linux 的快速 ARM 芯片的单板电脑一样，必须和树莓派做比较。由于这是第一款内置无线连接的 BeagleBone，最合理的比较是与最近发布的 Raspberry Pi 3 进行比较。

Pi 3 包括一个集成的无线芯片组，用于 802.11n 和蓝牙 4.1 连接。BeagleBone Green 无线有这个，但是也增加了 802.11 b 和 g 网络。这使得 BBGW 能够感知附近是否有人在使用微波炉——这对于我们经常听说的物联网来说是一个福音。

与 Pi 3 不同，BBGW 有两个 u.FL 连接器形式的附加天线连接。虽然 Pi 3 可以被黑客攻击来使用外部天线，但这不是心脏虚弱者的工作。小型、紧凑、低功耗的外置天线是任何无线网络连接处理范围或拥塞网络的理想解决方案。

### Grove 连接器

[![Grove](img/dd63730380ff490b8bb6e2e6b16f770e.png)](https://hackaday.com/wp-content/uploads/2016/05/grove.jpg)

The BeagleBone Green Wireless and Grove Base cape

BeagleBone Green Wireless 是一个 Seeed 接头，与最初的 BeagleBone Green 一样，在电路板边缘有 Grove 连接器。这些连接器分别为 Seeed Studio 的定制模块提供一条 I2C 总线和一条串行连接。

老实说，当谈到 Seeed 的 Grove 连接器时，我犹豫不决。一方面，试验板和杜邦电缆已经存在，有了 BeagleBone Black 上的两个 46 针接头，就没有什么不能接入 BeagleBone Black 的了。Grove connectors 的加入似乎是多余的，从最愤世嫉俗的角度来看，这仅仅是一个建立专有教育电子系统的尝试。

另一方面，对于当前的教育电子趋势，确实没有任何易于使用的插件模块系统。就在几年前，人们将带有 RS-442 的电路板插入 RJ45 插座。我们已经没有 DE-9 连接器了，更小、更容易使用的连接器很受欢迎，尤其是当连接器[仅为 0.15 美元/个](http://www.seeedstudio.com/depot/Grove-Universal-4-pin-connector-p-789.html)时。

此外，Grove 模块的智能完全取决于操作员。在 BeagleBone Green 上，有两个 Grove 连接器，一个用于 I2C，另一个用于串行。除了一些丝网印刷，这两个连接器之间没有区别。在 [Grove base cape](http://www.seeedstudio.com/depot/Grove-Base-Cape-for-Beaglebone-v20-p-2644.html) 上，使用 Grove 连接器有四种不同的实现方式:四个 I2C，四个数字 I/O，每个都有两个 GPIOs，两个专用于模拟输入的连接器，以及两个串行端口。这是通过普通电线连接大量设备的简单方法；它不是最用户友好的。

### 结论

BeagleBone Green Wireless 并没有什么新的东西。SoC 是相同的，当然每个 BeagleBone 中的 pru 都是非常非常快速的数字 I/O 的杀手级功能。增加 WiFi 很好，包括额外的天线连接器也很显著，但这不是 USB WiFi 加密狗不能处理的。

如果有的话，BeagleBone Green Wireless 是 BeagleBone 平台未来的一个信号。版本的数量，每个版本都有自己的小连接，是通往树莓派大教堂的集市。这对于任何开放硬件的爱好者来说都是令人鼓舞的，至少是工具棚中的另一个工具。