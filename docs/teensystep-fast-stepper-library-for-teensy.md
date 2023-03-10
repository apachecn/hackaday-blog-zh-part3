# TeensyStep——面向青少年的快速步进程序库

> 原文：<https://hackaday.com/2017/10/17/teensystep-fast-stepper-library-for-teensy/>

Teensy 平台很受黑客欢迎——这是理所当然的。Teensys 有 8 位和 32 位版本，硬件有面包板友好的足迹，有大量的 Teensy 库可用，它们也可以运行标准的 Arduino 库。想让很多 LED 闪烁吗？以非常快的更新速度？MIDI 怎么样？还是 USB-HID 设备？青少年可以处理任何你扔给它的东西。使用标准 Arduino 库，如 Stepper、AccelStepper 或 Arduino Stepper 库，可以轻松驱动电机。

但是如果你想以高的微步进速度移动多个电机，无论是独立的还是同步的，并且没有步进损失，这些标准库就成了瓶颈。[Lutz nigl]的新 [TeensyStep 快速步进器控制库](https://github.com/luni64/TeensyStep)在高速驱动步进器时提供了巨大的性能改进。它可与所有 Teensy 3.x 板配合使用，能够以微步进驱动器所需的高脉冲速率处理多个电机的加速同步和独立运动。

该库可用于以高达 300，000 步/秒的速度转动电机，在 1/16 微步进时达到令人难以置信的 5625 rpm。在下面的演示视频中，你可以看到他以 160，000 步/秒的速度推动两个马达，也就是 3000 转/分钟，两臂没有碰撞。电机可以独立或同步移动。同步运动使用 Bresenham 的直线算法，根据开始和结束位置规划电机运动。在进行同步移动的同时，它还可以独立运行其他电机。TeensyStep 库使用两个类对象。除了 56 字节的内存外，*步进器*类不需要任何系统资源。 *StepControl* 类需要一个 IntervallTimer 和两个 FTM (FlexTimer 模块)定时器通道。由于所有受支持的 Teensys 都实现了四个坑定时器和一个带有八个定时器通道的 FTM0 模块，因此使用仅限于同时存在的四个*步进控制*对象。查看[Lutz]的项目页面，获取一些性能数据。

作为比较，看看 8 位 Micros 的[更好的步进——这种方法使用 DMA 通道作为高速计数器，每次计数都向电机发送一个脉冲。](https://hackaday.com/2017/09/17/better-stepping-with-8-bit-micros/)

感谢[Paul Stoffregen]向我们透露了这个新图书馆的信息。

 [https://www.youtube.com/embed/Fzt75I_Zi14?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Fzt75I_Zi14?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

