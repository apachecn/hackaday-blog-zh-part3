# 用 FPGA 进行重力仿真

> 原文：<https://hackaday.com/2017/01/02/gravity-simulations-with-an-fpga/>

在传统的 CPU 上有效地模拟重力可能是一件困难的事情。所需的计算量随着模拟中粒子数量的增加而呈指数增长。这是一个适合并行处理的应用程序。

为了他们在康奈尔大学 ECE5760 的最终项目，[Mark Eiding]和[Brian Curless]决定使用 FPGA 来快速处理引力计算。这使得他们能够以每秒 10 帧的速度模拟 1000 个粒子。由于每个粒子都相互吸引，这相当于惊人的每帧一百万次平方反比运算！

该团队使用 Altera DE2-115 开发板来构建该项目。一般操作由 Nios II 处理器运行，该处理器处理 VGA 显示、加载初始条件并控制内存。FPGA 被用作重力计算的加速器，并且由于它并行运行所有操作，因此需要更少的存储器访问操作。

这个项目是一个很好的例子，说明了如何使用 FPGAs 为大规模并行任务创建强大的处理能力。查看这篇关于利用 FPGA 进行[排序的文章，这篇文章深入探讨了这个主题。休息后的视频。](http://hackaday.com/2016/01/20/a-linear-time-sorting-algorithm-for-fpgas/)

 [https://www.youtube.com/embed/L4tIfvVjNnI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/L4tIfvVjNnI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[感谢布鲁斯·兰德的提示]