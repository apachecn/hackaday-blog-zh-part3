# 通过玩马里奥黑掉 Flappy Bird

> 原文：<https://hackaday.com/2016/04/03/hacking-flappy-bird-by-playing-mario/>

这是黑客和游戏的杰作！[Seth Bling]在《超级马里奥世界》( SMW)中执行了一次代码注入黑客攻击，不仅使游戏出现故障，而且重新编程以玩“Flappy Bird”的精简版。他没有使用一组 JTAG 探测器，而是使用游戏自己的控制器。

很明显，有一群人在从游戏内部破解超级马里奥世界，其中一些黑客使用修改过的控制器来执行代码序列。关于我们的黑客，最疯狂的事情是[Seth]完全是手工完成的。[完整的笔记可以在这里找到](https://docs.google.com/document/d/1TJ6W7TI9fH3qXb2GrOqhtDAbVkbIHMvLusX1rTx9lHA/edit)，但是我们会为你总结一下程序。或者你可以去看下面的视频。真的很不可思议。

首先，有一个"[加电增量故障](https://www.youtube.com/watch?v=TqK-2jUQBUY)"让你让马里奥进入一个不确定的加电状态。然后[Seth]执行了另一次黑客攻击来停止游戏的计时器，这样他就有足够的时间来玩了。

[![2016-03-30-123215_1366x1792_scrot](img/fedeb549ef7e92846caf45941ffdd7e8.png)](https://hackaday.com/wp-content/uploads/2016/03/2016-03-30-123215_1366x1792_scrot.png) 从这里，他可以通过将马里奥放在正确的位置并丢下一个蘑菇，将字节直接输入 RAM。Mario 的 x 坐标值被写入内存。[Seth]必须将 Mario 的位置与背景进行比较，从而使他准确地出现在正确的像素上。这是如此令人难以置信的乏味，需要如此精确，以至于他输入的前几个字节的代码是一个显示马里奥在硬币计数器中的位置的例程。你可以看到这个在 3:30 左右工作。

下一个技巧是添加一个引导加载程序，让他通过自旋跳跃输入字节。这让他可以相对容易地输入字节——移动到硬币显示屏上指示的正确位置，然后旋转跳跃。到目前为止，图形都是乱糟糟的，但是他在字节级上实时修补一个正在运行的系统，所以你还能期待什么呢？bootloader 最酷的功能？最后的校验和验证代码，以便您可以在代码输入阶段重新开始，而不是重新做半个小时的“上-上-下-下-左-右-左-右-B-A”。

最后，一个基本的“Flappy Bird”游戏被加载到系统中。[Seth]只花了一个小时就完成了这件事，但链条的早期部分非常关键，他不能犯任何错误。下一次，当你坐在你的反汇编器/调试器前敲退格键的时候，想象一下你不得不从头开始。这是没有网络的高空黑客。太神奇了！

感谢[gudenau]和[Le Samourai]的提示！

 [https://www.youtube.com/embed/hB6eY73sLV0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hB6eY73sLV0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

