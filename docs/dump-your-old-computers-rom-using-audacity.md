# 使用 Audacity 转储你的(旧)计算机的 ROM

> 原文：<https://hackaday.com/2016/04/12/dump-your-old-computers-rom-using-audacity/>

如果你有一个旧的计算器，Commodore 64 或任何其他使用磁带录音机存储和检索数据的设备，你可能也有一堆磁带，对不对？好吧，你现在可以把它们扔掉(或者以惊人的价格卖给怀旧的收藏家)，因为你可以很容易地把它们转交给 Audacity，解码它们，并把它们存档在一个更理智的媒体上。

在[Kai]的案例中，计算机是一个夏普袖珍计算机系统，在他的文章中有许多特定于该特定系统的细节。如果这适用于你，去读吧。特别是，你会很高兴地发现[袖珍工具](http://pocket.free.fr/html/soft/pocket-tools_e.html)是一个软件套件，将编码和解码文件之间的夏普二进制格式和音频。一路上，我们发现[也有类似的卡西欧袖珍电脑](http://www.mvcsys.de/doc/casioutil.html)的工具。

对于更通用的方法，比如如果你试图从使用 1200/2400 Hz FSK 编码的[更标准的](https://en.wikipedia.org/wiki/Kansas_City_standard)计算机上转储和加载数据，[这个 Python 库可能有用](http://www.dabeaz.com/py-kcs/index.html)，或者你可以在你选择的平台上自己实现 [Goerzel 算法](http://hackipedia.org/Algorithms/DSP/html/Goertzel_algorithm.htm)。但是，如果您已经想到了一种特定的二进制格式，那么您就必须自己去做这项繁重的工作。

有人还在使用这些音频数据编码吗？我们知道业余无线电的 [APRS](http://hackaday.com/2015/03/24/aprs-tracking-system-flies-your-balloons/) 系统运行在两种音调上。还有什么？如今，您为什么以及何时会以这种方式传输数据？

via [阿达果博客](https://blog.adafruit.com/2016/03/30/dump-ram-and-rom-on-sharp-pc-15001600s-using-audacity-software/)！