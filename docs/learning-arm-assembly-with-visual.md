# 带视觉的学习臂组件

> 原文：<https://hackaday.com/2017/12/28/learning-arm-assembly-with-visual/>

如果你想真正了解计算机是如何工作的，学习汇编是非常重要的。对于有兴趣学习 ARM assembly 的人来说，VisUAL 是一个非常强大的 ARM 模拟器。

![](img/fa5bb0eedd1ea6787a588e88266b3f5e.png)

The GUI: A simply program to ADD two numbers

除了支持 ARM 指令的大型子集之外，CPU 还通过一系列精心制作的指导性动画进行仿真，这些动画有助于可视化进出寄存器的数据流、对标志所做的任何更改以及所采取的任何分支。它还包含非常有用的动画，可以帮助你掌握一些更复杂的指令，比如移位和堆栈操作。

由于它是专门设计用作[伦敦帝国理工学院的教学工具，](https://www.imperial.ac.uk/)GUI 非常友好，所有的语法错误都被突出显示，并且还显示了正确语法的示例。

![](img/08ea12132c14916caae40acb4d4c7a77.png)

Branch visualisation, credits: [VisUAL homepage](https://salmanarif.bitbucket.io/visual/index.html)

您还可以做任何模拟器都会做的事情，比如单步执行、设置断点以及在不同的基础上查看数据。它甚至警告你任何可能的无限循环！

也就是说，携带如此奢侈的 GUI 是有代价的；消耗几十万个周期的程序占用了太多的 RAM，应该在支持的无头模式下运行。