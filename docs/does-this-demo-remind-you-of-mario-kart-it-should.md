# 这个演示是否让你想起了马里奥赛车？应该的！

> 原文：<https://hackaday.com/2017/02/16/does-this-demo-remind-you-of-mario-kart-it-should/>

这里有一个由[Yianni Kostaris]用汇编语言编写的看起来很光滑的 VGA 演示；它是一个 16MHz 的 ATmega2560 的 VGA 输出，不涉及外部芯片。如果你从《超级马里奥赛车》的外观中获得了一些灵感，这是有充分理由的。该演示实现了超级任天堂的[模式 7](https://en.wikipedia.org/wiki/Mode_7) 图形的一种形式，它允许背景被有效地纹理映射、旋转和缩放以获得 3D 效果。它被用于赛车游戏(如超级马里奥赛车)，但也在许多其他游戏。下面嵌入了演示视频。

[Yianni]一年前发布了原始演示，但最近才添加了关于它是如何完成的详细技术信息。AVR 直接输出 VGA 信号，分辨率为 100×120，256 色，以 60 fps 的速度快速传输。AVR 本身没有以任何方式修改或超频——它运行在完全正常的 16MHz，93%的时间用于处理中断。尽管分享了如何做到这一点的细节，[Yianni]还没有发布任何代码，但告诉我们这个演示是另一个仍在进行中的项目的分支。这值得继续关注，因为很明显(Yianni)知道他的东西。

 [https://www.youtube.com/embed/ZpPd0pdQ3dE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZpPd0pdQ3dE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



VGA 在台式电脑领域可能已经今非昔比，但它是黑客项目的沃土。我们已经看到一个 Arduino [驱动一个 VGA 显示器](http://hackaday.com/2016/12/08/vga-monitor-becomes-drawing-toy/)就像它是一个蚀刻素描，以及如何 [bit-bang VGA 在 1k](http://hackaday.com/2016/12/08/bitbanging-vga-fits-in-under-1-kb/) 以下。