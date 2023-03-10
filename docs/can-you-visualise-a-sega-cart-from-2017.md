# 你能想象 2017 年的世嘉车吗？

> 原文：<https://hackaday.com/2017/08/31/can-you-visualise-a-sega-cart-from-2017/>

Sega Genesis，或者如果你不是来自北美的话，Mega Drive，并不完全是今年夏天最热门的新主机，但在推出 29 年后，它仍然有一大批追随者。粉丝范围从复古声波爱好者到硬核 chiptune 作曲家，今年，Catskull Electronics 发行了一张带有相当特殊功能的盒式唱片 [Genesis 编译专辑。](https://catskull.net/ym2017)

该拾音器配有一个 8×8 的 LED 矩阵，可以显示来自控制台的音频。它们由数据和地址线以及一些缓冲器和 74 系列粘合逻辑的组合来控制，使它们一起工作。特别注意确保 LED 矩阵不仅仅响应总线上的所有活动，尽管有一天在 90 年代的控制台上看到一些闪光灯可能会很酷。

每一行发光二极管连接到地址线上，每一列连接到数据线上。这是一个相当基本的多路复用设置，每个 LED 实际上只点亮几分之一秒，但快速扫描显示器会产生持久的显示。图像数据以 8×8 子画面的形式存储在系统 RAM 中，并根据 Genesis 音频子系统中每个通道的音量进行更新。

该团队希望在未来发布 ROM 代码，以激发模仿设计，这有可能在未来催生更多的 Genesis cart 版本。我们期待看到社区提出的其他内容。如果你是《创世纪》的铁杆粉丝，[也有其他方法来听这些经典歌曲](https://hackaday.com/2017/02/17/sega-genesis-chiptunes-player-uses-original-chips/)。