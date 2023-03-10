# FPGA 上的 Amstrad

> 原文：<https://hackaday.com/2017/01/06/amstrad-on-an-fpga/>

如果你来自美国，到了一定年龄，你很可能拥有某种形式的 Commodore 计算机。在美国以外，同样的人群也可能拥有一辆 Amstrad。基于 Z80 的电脑以玩游戏而闻名。[Freemac]在 NEXYS2 演示板上使用 Xilinx FPGA 实现了一个有效的 Amstrad CPC 6128。

wiki 帖子有点长，但它涵盖了如何复制这一壮举，并给出了有关设计的技术细节。它还概述了从简单的 Z80 仿真开始到更复杂的尝试的开发过程。你可以在下面看到这个设备的视频。

那个时代的计算机经常为了省钱和在有限的马力下工作而做出妥协。例如，Sinclair 计算机在你打字时会闪烁其视频，这是出了名的，因为 CPU 无法同时驱动显示器和读取键盘。Amstrad 限制了 CPU 对内存的访问，以避免与视频硬件发生冲突，因此 4 MHz 的 CPU 被有效地限制在 3 MHz 以上。与消耗几十或几百兆内存的现代网络浏览器相比，探索这些旧架构可以向您展示一种不同的思维方式。

我们以前见过 Amstrad 的克隆体。我们也看到了[一个真正的 Amstrad 和一个 iPod Shuffle](http://hackaday.com/2005/11/21/amstrad-ipod-shuffle-tape-drive/) 的邪恶结合，iPod 代替了一个数据卡带。想知道 FPGA 模拟器能不能读磁带？

 [https://www.youtube.com/embed/Z8FB_eIy8LY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Z8FB_eIy8LY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

