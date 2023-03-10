# [Ken Shirriff]揭开 BeagleBone I/O 的神秘面纱

> 原文：<https://hackaday.com/2016/08/19/ken-shirriff-demystifies-beaglebone-io/>

如果你曾经花了一点时间钻研与当代微处理器或微控制器上的 I/O 引脚交谈的裸机，你就会知道这并不总是适合胆小的人。许多不同的功能可以在一个物理引脚后面复用，一旦你透过操作系统的外衣看硬件，你精心安排的时间可能会在瞬间脱轨。由于这些原因，我们大多数人会利用他人的成果，使用库或虚拟文件系统路径提供的抽象。

如果你有足够的好奇心去窥视你的主板 I/O 的内部，那么你可能会发现[Ken Shirriff]的最新博客文章，其中[他探索了一个 BeagleBone Black](http://www.righto.com/2016/08/the-beaglebones-io-pins-inside-software.html) 上的引脚背后的软件堆栈。虽然它的细节是一个设备的细节，但它提出的观点与许多其他类似的电路板相关。

他首先研究了通过虚拟文件系统路径访问 Beagle Bone 的 I/O 行的最简单方法。然后，他解释了为什么如此严重地依赖操作系统会导致严重的计时问题，并继续探索引脚背后的物理寄存器。然后，他讨论了不同引脚功能的多路复用，然后解释了 Linux 设备树在保持操作系统与硬件联系方面的作用。

对于一些黑客读者来说，这都是旧闻了，但是可以肯定地说，BeagleBone Black 等电路板的许多用户将永远不会看到使用 I/O 引脚的安全抽象方法之外的东西。因此，这篇文章应该为芯片硬件新手提供一个有趣的教育，并且可能仍然包含一些对更高级用户的有用信息。

这些年来，我们在 Hackaday 看到了很多[Ken]的工作，大部分是在逆向工程领域。其中一些是他对 TL431 基准电压源的[解释，对 741 运算放大器](http://hackaday.com/2014/05/26/ken-shirriff-explains-the-tl431/)的完整[检查，以及他对 20 世纪 70 年代辛克莱科学计算器](http://hackaday.com/2015/10/31/a-peek-under-the-hood-of-the-741-op-amp/)的[逆向工程。](http://hackaday.com/2013/08/30/ken-shirriff-completely-reverse-engineers-the-1974-sinclair-scientific-calculator/)

我们感谢[Fustini]对这个故事的提示。

BeagleBone 黑色图片:BeagleBoard.org 基金会[CC BY-SA 3.0]，via [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Beaglebone_Black.jpg?uselang=en-gb) 。