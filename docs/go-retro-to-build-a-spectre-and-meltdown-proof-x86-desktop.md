# 追溯过去，构建一个不受 Spectre 和 Meltdown 影响的 X86 台式机

> 原文：<https://hackaday.com/2018/01/07/go-retro-to-build-a-spectre-and-meltdown-proof-x86-desktop/>

[Yeo Kheng Meng]有一个问题:现代 Linux 内核仍然支持的最古老的 x86 处理器是什么？此外，这种处理器实际上可以使用现代软件吗？这个问题肯定涉及到实验，盯着 BIOS 配置的蓝屏深渊，以及编译你自己的内核。考虑到 Linux 在 2012 年放弃了对 386 的支持，显而易见的答案是 486。这一假设得到了验证，结果是惊人的。的确，你可以在古老的桌面上安装一个现代的 Linux。

这个项目是上个月在一个超级愚蠢的黑客马拉松上开始的，在那里(Yeo)和(惠晶)在一台 1993 年的 IBM PS/1 台式机上安装了该死的小型 Linux。硬件包括一个运行在 133MHz 的 AMD 486 克隆，64 MB 的 RAM，一个 48x IDE CDROM 驱动器(哇！)、软盘仿真器、声霸、10Mbps 以太网卡和 CompactFlash 到 IDE 适配器。不管怎么说，这是一辆 1993 年的破车，在当时比一辆车还贵。硬件可以工作，但是你能在它上面运行一个现代的 Linux 内核吗？

[Yeo]决定安装 Gentoo x86 最小安装，但是健全性和时间限制意味着在 486 上编译内核是不可能的。这是在对所有驱动器进行分区、验证所有编译参数并配置内核本身之后，在现代 Thinkpad 上完成的。引导加载程序是 LILO (Grub2 没有工作)，但在大多数情况下，这完全是运行在 25 年前的机器上的现代软件。在 GitHub 上可以找到成为 486 [上的 a /g/entooman 的逐步说明。](https://github.com/yeokm1/gentoo-on-486)

整个(无聊的)开机过程可以在下面的视频中看到。这种构建的一个有趣的应用是 486 不支持乱序执行，这使得它完全不受 Meltdown 和 Spectre 攻击的影响。这是一个令人印象深刻的回溯性成就，现在再及时不过了。

 [https://www.youtube.com/embed/4qSziR6sD8Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/4qSziR6sD8Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

