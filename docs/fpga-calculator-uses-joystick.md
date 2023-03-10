# FPGA 计算器使用操纵杆

> 原文：<https://hackaday.com/2018/02/28/fpga-calculator-uses-joystick/>

FPGAs 非常有趣，但有时你需要一些入门项目。这些项目可能是你可以用 CPU 做的事情，但是你必须从某个地方开始。[LambdaPI]最近分享了一个使用 FPGA 创建的 4 位计算器[，你可以在下面的视频中看到它。](https://github.com/LambPi/Calculator)

该计算器使用 Papilio FPGA 板和 LogicStart 附件板进行显示和开关。Papilio 通常使用基于原理图的输入和 Arduino 代码，但[LambdaPI]使用 VHDL。您在 8 个开关上输入两个 4 位数字，然后操纵杆选择四种操作之一(加、减、乘、除)。

在代码内部，您会看到 FPGA 同时完成所有四种计算。操纵杆只是选择输出到显示器。每个模块还单独解码 led，这是一个有趣的设计选择。从负面来看，它复制了大量代码，但不需要用除法(显示为定点十进制数)来改变格式。

我们已经看到 Papilio 板作为 [128 MHz Z80 CPU](https://hackaday.com/2014/05/01/a-z80-retro-microcomputer-for-the-papilio-pro-fpga-board/) 执行任务。或者你可以用 [one 来制作一个流光溢彩](https://hackaday.com/2014/12/16/fpga-ambilight-clone-packs-a-ton-of-features/)。然而，作为第一个项目，这个计算器真的可以满足要求。如果你没有任何硬件，你可以尝试使用 [EDA 操场](https://hackaday.com/2015/07/21/learn-fpgas-in-your-browser/)。

 [https://www.youtube.com/embed/MzP1AcQhk08?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MzP1AcQhk08?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

