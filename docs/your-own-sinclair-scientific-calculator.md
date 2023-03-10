# 你自己的辛克莱科学计算器

> 原文：<https://hackaday.com/2018/06/22/your-own-sinclair-scientific-calculator/>

我们以前多次谈到过辛克莱科学计算器，对我们中的一些人来说，这是我们的第一个科学计算器。如果你找不到你的或者你从来没有过，现在你可以使用 Arduino——或者别的什么——借助[Arduino Enigma]来建造你自己的。下面有一个视频，这个项目在 Hackaday.io 上的[主页完美地描述了这一切:](https://hackaday.io/project/91895-sinclair-scientific-calculator-emulator)

> 肯·希尔里夫对辛克莱科学计算器内部的原始芯片进行了逆向工程，提取了它的 320 指令程序，并编写了一个在线模拟器。该项目将使用 Javascript 编写仿真器移植到 Arduino Nano，并将其连接到定制的 PCB。结果是一个对象的行为就像最初的计算器一样，有它自己的特点和问题。将圆周率计算为 arctan(1)*4 得出的值为 3.1440。
> 
> 仿真器的设计特别小心，以匹配
> 原始计算器的执行速度，对于涉及小角度的三角函数，执行速度从可接受到糟糕不等。

奇怪的是，这个计算器最初是对 KIM-1 UNO 的黑客攻击。然而，六次电路板修订使布局发生了很大变化，使仿真在软件和物理上都越来越精确。如果你想近距离看看原版的辛克莱[，我们把它拆了。](https://hackaday.com/2017/11/01/a-teardown-with-a-twist-1975-sinclair-scientific-calculator/)

KIM-1 UNO 板注入了很多活力。我们把它用作时钟和 T2 1802 模拟器。Oscar 甚至用 1802 代码为[添加视频输出](https://obsolescenceguaranteed.blogspot.com/2017/08/the-uno1802-cosmac-elf-for-15-in-parts.html)。

 [https://www.youtube.com/embed/S6wooBknsMs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/S6wooBknsMs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

