# 火腿评论小货车

> 原文：<https://hackaday.com/2018/05/06/ham-reviews-minivna/>

[KB9RLW]想要建立一个矢量网络分析仪(VNA)，但后来意识到他可以购买一个现成的，几乎没有成本，这将是只有几年前。顺便说一下，这里的网络是一个电气网络，而不是计算机网络。您可以使用 VNA 来表征不同频率下的组件、电路、天线甚至馈线。miniVNA Pro 很经济，可以运行 1 MHz 到 3 GHz 的电路。你可以在下面的视频里看到[的评测。](https://www.youtube.com/watch?v=tW14Hxm1BEY)

有几种方法可以实际创建 VNA，但在概念上，它是一个扫描发生器、一个检波器，也是一种在扫描中绘制每个频率下的响应的方法。例如，您可能会期望谐振频率在谐振时显示峰值，带阻滤波器显示低点。

该设备有趣的一点是它使用 Java 软件。这意味着它不太在乎你想用什么平台。该软件可以同时显示两个不同的图，因此[Kevin]将其连接到他的 20 米天线，并显示如何绘制目标频率周围的 SWR 和阻抗。

仪器可以通过 USB 供电，使用与连接 PC 相同的电缆。然而，它也有一个内部充电电池。该电池通过 USB 充电，可以通过蓝牙操作设备。我们可以想象，当你想爬上一座塔，并将其直接连接到天线上时，只要你在 PC 的蓝牙范围内，这将是非常方便的。还有一个手机应用程序，所以你可以走这条路，如果你喜欢的话，[凯文]展示了与 Android 兼容的设备。当然，你可以在你的腰带上挂一个树莓皮，然后使用 WiFi 让地面远程桌面上的人进来进行测量。很多可能性。

如果你想自己卷，[那当然有可能](https://hackaday.com/2016/08/13/a-vna-on-a-200-euro-budget/)。如果你想过得便宜一点，有[更便宜的选择](https://hackaday.com/2018/03/29/putting-a-poor-mans-vector-analyzer-through-its-paces/)。

 [https://www.youtube.com/embed/tW14Hxm1BEY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/tW14Hxm1BEY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

