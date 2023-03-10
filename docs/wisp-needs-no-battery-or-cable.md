# WISP 不需要电池或电缆

> 原文：<https://hackaday.com/2016/05/01/wisp-needs-no-battery-or-cable/>

物联网或任何嵌入式设备的一个问题是如何获得电力。电池比以往任何时候都好，电路是低功耗的。但是你最终还是要更换电池或者给电池充电。不是所有东西都能插到墙上，燃料电池也需要耗材。

华盛顿大学的研究人员正在转向一种收获方法。他们的开源 WISP 板有一个传感器和一个从 RFID 阅读器获取能量的 CPU。为了在通信过程中节省电力，该设备反向散射传入的无线电波，这意味着它在传输过程中不会消耗大量的自身电力。

大新闻是，代尔夫特大学贡献了代码，允许 WISP 无线重新编程。你可以在下面看到一个关于创新的视频。源代码在 [GitHub](https://github.com/jettan/boot_wisp5) 上。以前，WISP 必须连接到 PC 才能接收新的软件加载。

当然，RFID 标签已经从 RFID 阅读器获取能量。然而，普通的 RFID 标签没有任何处理能力或传感器输入。WISP 有一个 16 位的 CPU。目前正在开发第五版。还有一个版本的[可以与现代智能手机和其他设备中常见的 NFC 读卡器](https://nfc-wisp.wikispaces.com/home)接口。

也有类似的装置试图从周围来源(例如无线电和电视广播)获取能量。没有电池的一个很大的好处是，设备可以放在他们够不到的地方。例如，一栋建筑可以在混凝土中灌注传感器，检查员可以为其供电并进行无线读取。显然，能够无线更新这样的设备将是一个很大的好处，因为你不能取回设备来连接电缆(或电池)。

窃取权力并不是一个新的想法。我们之前已经研究过热能收集技术，以及从热水龙头中窃取热量的一氧化碳传感器 T2。话说回来，你也可以[利用人体的力量](http://hackaday.com/2013/03/07/human-powered-emergency-cell-phone-charger/)(不需要矩阵)。

 [https://www.youtube.com/embed/rvtyZIPyXMs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rvtyZIPyXMs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

