# 为大义重编蓝牙耳机

> 原文：<https://hackaday.com/2017/01/30/reprogramming-bluetooth-headphones-for-great-justice/>

像许多大规模生产的消费品一样，事实证明，许多不同品牌的蓝牙耳机的内部工作原理是相同的。一个常见的蓝牙模块是 CSR8645，[lorf]意识到它相当常见，而且(更重要的是)相当容易修改。[lorf]能够组装一个工具包[来重新编程几乎所有这些耳机](https://github.com/lorf/csr-spi-ftdi#csr-chips-supported-by-programmer)中的蓝牙模块。

这个提示来自于[Tigox]，他已经很好地使用了[lorf]的软件。使用该工具包，他能够通过 USB 连接到他的电脑上对自己的蓝牙耳机进行重新编程。下载并运行[lorf]的程序后，他能够修改设备的名称，更重要的是，能够调整麦克风的增益行为，从而获得更加愉悦的用户体验。

此外，新的工具包可以将定制的 rom 闪存到 CSR 蓝牙模块。这开启了各种可能性，包括将一套廉价耳机用于听音乐之外的其他目的的可能性。按钮和麦克风可以重新用于几乎任何可以想象的任务。当然，你也许可以找到更便宜的蓝牙设备来改变 T1 的用途，但是如果你只是需要调整耳机的设置，那么这个方法会更有用。

[专题和缩略图[图片来源](https://commons.wikimedia.org/w/index.php?curid=40666148)JLab Audio LLC–jlabaudio.com，CC BY-SA 4.0]