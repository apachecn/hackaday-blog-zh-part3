# 完全用 Ada 语言编写的笔式绘图仪固件

> 原文：<https://hackaday.com/2016/06/09/pen-plotter-firmware-written-completely-in-ada/>

[Fabian Chouteau]用 CD-ROM 部件建造了一个绘图仪[。你说打哈欠？除了是一个美丽的身体构造，这一个有一个转折。他自己用 Ada 语言编写了整个项目的软件和固件。](http://blog.adacore.com/make-with-ada-arm-cortex-m-cnc-controller)

Ada 目前在我们的古怪编程语言列表中排名第二，应该对嵌入式编程有用。它是模糊的 Pascal-y，但是有一些现代的面向对象的变化。它是为安全关键的实时嵌入式系统(由美国国防部)开发的，用于飞机、火箭和法国 TGV 列车等。如果这听起来对你的项目来说有些过分，那么[Fabian]的项目表明它仍然非常容易处理。

在[他的 GitHub](https://github.com/Fabien-Chouteau/ACNC) 中，他重新实现了 [GRBL](https://github.com/grbl/grbl) G 代码生成器，然后为其编写了一个 GUI 前端。在他的文章中，他提到固件及其前端模拟器使用*完全相同的代码*，这是一个很好的技巧，并保证从模拟设备转移到真实设备时不会出现(固件)意外。

我们迅速寻找 Ada 资源，找到了:[GNU Ada 编译器 GNAT](http://gcc.gnu.org/wiki/GNAT) 及其衍生工具: [GNAT for ARM](http://libre.adacore.com/tools/gnat-gpl-for-bare-board-arm/) (STM32 风格) [ARM-Ada](https://sourceforge.net/projects/arm-ada/) (LPC21xx 风格) [AVR-Ada](https://sourceforge.net/projects/avr-ada/?source=recommended) 和 [MSP430-Ada](https://sourceforge.net/projects/msp430ada/?source=recommended) 。

有人在嵌入式工作中使用 Ada 吗？我们很想听听你的想法。

 [https://www.youtube.com/embed/uXfkWCUyjM8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/uXfkWCUyjM8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

