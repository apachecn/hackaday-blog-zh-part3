# 用 DIP 开关读出 EPROM

> 原文：<https://hackaday.com/2018/01/18/reading-out-an-eprom-with-dip-switches/>

如今，无论是微控制器的内部闪存还是一些外部 EEPROM，我们都过于沉迷于向永久存储器中写入和擦除数据的舒适方式。诚然，这些记忆技术并不算新，但它们源于一个时代，当时它们的前辈不得不沐浴在紫外线下，以便为新事物腾出空间。[Taylor Schweizer]最近偶然发现了一些石英窗装饰的芯片，很想知道里面储存了什么。受*停止并着火*、[中 BIOS 逆向工程场景的启发，他最终构建了自己的简单阅读器来显示 EPROM 的内容](http://learn-cnc.com/uv-eraseable-memory-fun-old-tech/)。

他用的 2732 是标准的 EPROM，有 32 千比特的内存。两个引脚(芯片使能和输出使能)用作主控制接口，而 12 个地址引脚选择存储在芯片内部 4K x 8 排列中的数据，以在 8 个数据输出引脚上输出。你当然可以将 EPROM 连接到一个微控制器上，并通过串行线发送你所读取的数据，但是[Taylor]选择了一种更具动手能力的方法，让他以手动方式读出数据。他简单地使用一组 DIP 开关来设置地址和控制引脚，并添加了一排 led 作为显示器。

正如你在休息后的视频中看到的，用这种方式读出整个 EPROM 将是一个相当乏味的任务。如果你真的想读出内容，你可以看看[一种基于微控制器的解决方案，通过串行线](https://hackaday.com/2012/09/10/2708-eprom-dumper/)发送数据。

 [https://www.youtube.com/embed/B0Xulae9gtA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/B0Xulae9gtA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

