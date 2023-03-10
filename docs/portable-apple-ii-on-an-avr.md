# AVR 上的便携式 Apple II

> 原文：<https://hackaday.com/2016/12/19/portable-apple-ii-on-an-avr/>

Apple II 是第一批家用电脑之一。它由史蒂夫“沃兹”沃兹尼亚克设计，使用 MOS technologies 6502 处理器，一种运行速度约为 1 MHz 的 8 位处理器。[max story]写了他的学士论文，关于在 AVR 1284 上用软件模拟 6502，并提出了一个带屏幕和键盘的手持原型 Apple II。

![pic_15](img/436e05a375b8cb641b5c1038de1a094f.png)

Prototype on veroboard

最初，[maxstrauch]想建造一个 NES，它使用相同的 6502 处理器，但他计算出 NES 的图像处理单元对 AVR 来说太复杂了，所以他开始模仿 Apple II。它并不完全如此——它只能引用 12K 的内存，而不是原始版本上的 64K，所以高分辨率图形模式，因此，许多游戏都无法工作，但低分辨率模式与基本模式(Integer BASIC 和 Applesoft BASIC)一样好。)

[Maxstrauch]在其论文中详细介绍了 6502，并在另一份文档中概述了该项目的情况。第三份文档中有他用来构建仿真器的原理图。他的论文详细介绍了 6502，以及他如何将其映射到 AVR 微控制器。建筑本身也令人印象深刻。在 veroboard 上完成，这个建筑有一个显示器，键盘和一个小扬声器，以及一个用于读取和存储数据的微型 SD 卡。对于更多的 6502 项目，请查看 [Dis-Integrated 6502](https://hackaday.com/2016/05/16/a-dis-integrated-6502/) 以及[这个自制 6502](https://hackaday.com/2012/05/10/your-guide-to-building-a-homebrew-6502-computer/) 指南。

 [https://www.youtube.com/embed/yMmLo94A9eU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/yMmLo94A9eU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

