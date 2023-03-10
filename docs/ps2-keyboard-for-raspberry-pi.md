# 树莓 Pi 的 PS/2 键盘

> 原文：<https://hackaday.com/2016/01/14/ps2-keyboard-for-raspberry-pi/>

很多人会烤蛋糕。算是吧。如果我们有蛋糕配料，大多数人都能烤蛋糕。从头开始做蛋糕是一个不同的命题。当然，你知道这是可能的，但在现实生活中，我们大多数人只是得到一盒蛋糕粉。树莓派不是蛋糕(甚至不是馅饼)，但是你可以对它做同样的观察。你知道 Raspberry Pi 只是一台 ARM 计算机，你可以在不运行现有操作系统的情况下对它进行编程，但实际上你不会这么做。这就是为什么看那些接受这个挑战的人很有趣。

[Deater]正在编写自己的 Pi 操作系统，他面临一个令人生畏的问题:键盘输入。通常，您将 USB 键盘插入 Pi(或连接到 Pi 的集线器)。但是这仅仅是因为 Linux USB 堆栈和驱动程序的存在。仅仅是让简单的键盘输入为测试和调试工作，就需要大量的代码。这就是为什么[Deater]为 Pi 创建了[一个 PS/2 键盘接口。](http://www.deater.net/weave/vmwprod/hardware/pi-ps2/)

即使您没有编写自己的操作系统，您也可能会发现使用 PS/2 键盘来释放 USB 端口很有用，或者您可能想在没有 USB 适配器的情况下连接漂亮的 M 型键盘。PS/2 键盘使用相对简单且易于理解的时钟和数据协议。唯一真正的问题是将 5V PS/2 信号转换为 Pi 的 3.3V 信号(当然反之亦然)。

代码位干扰 PS/2 时钟和数据，不像其他一些项目占用 UART(不允许使用串行控制台进行开发)。[Deater]说只要稍加修改，代码就可以在鼠标上运行。面临的挑战是在未知中断延迟的情况下处理数据速率。顺便说一下，[Deater's] PCB 上的 USB 端口允许你用适配器连接一些退回到 PS/2 模式的 USB 键盘。不能随便插个 USB 键盘进去。

在之前，我们已经介绍过 [PS/2 与不同平台的接口，甚至看到过](http://hackaday.com/2011/09/23/interfacing-with-a-ps2-keyboard/)[将键盘转换成鼓机](http://hackaday.com/2014/07/31/ps2-synth-will-knock-you-off-your-broom/)。下面可以看到一个关于树莓 Pi 接口构建的视频。

 [https://www.youtube.com/embed/p0G-3RjAh3I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/p0G-3RjAh3I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

