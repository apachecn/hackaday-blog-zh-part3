# Arduino 草图:下一代

> 原文：<https://hackaday.com/2016/09/22/arduino-sketch-the-next-generation/>

你的第一个 Arduino 程序是什么？可能是 LED 闪光灯——这似乎是微控制器的“你好世界”。你可能很快就转移到更复杂的事情上了。在某种程度上，事情变得更加困难，因为 Arduino 缺乏操作系统。

Arduino 上可以运行一些操作系统。它们不像 Windows 或 Linux 那样功能齐全，但它们允许您运行多个任务，这些任务既相互隔离(在某种程度上)，又有一种协作方式(即同步、共享数据和资源，等等)。一个这样的操作系统就是 [ChibiOS](https://github.com/greiman/ChibiOS-Arduino) 。它可以在基于 AVR 和 ARM 的设备上运行。你可以在[主页](http://www.chibios.org/dokuwiki/doku.php?id=start)和其他端口找到关于整个项目的文档。

采用新操作系统的问题总是在于如何开始。[ItKindaWorks]已经开始了一个关于使用 ChibiOS 的视频系列，到目前为止已经发布了三期(见下文；一篇是关于入门的，另外两篇涉及消息传递、互斥和优先级)。

如果你想跟随视频，代码可以在 [GitHub](https://github.com/ItKindaWorks/sketches/tree/master/ChibiOS/ChibiOS_03) 上找到。我们不确定他是否在计划更多的视频，但是这些足够让你开始了。

根据 ChibiOS 项目，它们比许多常见的类似操作系统都要好，因为它们的静态设计(可以让处理器进入睡眠状态，而不会导致问题)。它们还支持真正的线程，而不是简单的任务，这意味着您可以动态地创建和销毁线程，并轻松地同步线程。

如果你正在构建一个复杂的软件，它需要多件事情同时发生，那么拥有一个操作系统会让生活变得容易得多。我们已经看到了使用 ChibiOS 的例子，从[电机控制](https://hackaday.com/2016/02/04/adding-position-control-to-an-open-source-brushless-motor-driver/)到 [MIDI 播放器](https://hackaday.com/2015/09/13/discovery-midi-sample-player/)。如果你环顾四周，除了 ChibiOS，还有很多其他的[选择](https://hackaday.com/2015/11/14/object-oriented-state-machine-operating-system-goes-open-source/)。

 [https://www.youtube.com/embed/JXy86GrjVso?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/JXy86GrjVso?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/ub2ZEaIWw8o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ub2ZEaIWw8o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/U0zAwnfWcHM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/U0zAwnfWcHM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

