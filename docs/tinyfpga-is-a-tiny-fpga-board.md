# TinyFPGA 是一种微型 FPGA 板

> 原文：<https://hackaday.com/2017/07/31/tinyfpga-is-a-tiny-fpga-board/>

我们最近注意到来自[Luke Valenty]的 TinyFPGA A 系列板的开源设计。这种微型板的尺寸为 18 毫米乘 30.5 毫米，并且是试验板友好型的。如果您需要额外的容量，您可以选择支持网格 Mach XO2-256 或 XO2-1200 的主板。

这些板在侧引脚和顶部接头上都有 JTAG 接口，可以方便地插入 JTAG 加密狗进行编程。当这些微小的芯片被埋在这样的分线板中时，工作起来就容易多了。带有 led 和其他 I/O 设备的更大的电路板有利于学习，但它们并不总是有利于集成到更大的项目中。TinyFPGA 板很容易在您正在制作原型或进行小规模生产的设备中工作。

文件在 [GitHub](https://github.com/tinyfpga/TinyFPGA-A-Series) 上。根据该项目的[主网站](http://tinyfpga.com/)，这是“A 系列”,因为即将推出的“B 系列”主板使用 USB 而不是 JTAG，并将使用 Lattice ICE FPGA 设备。

板上的元件采用 0603 和 QFN32 封装。[Luke]建议使用焊锡膏、锡膏和烤箱，但是这些尺寸的元件可以通过练习手工焊接。

如果你想了解 FPGAs 的方式和原因，我们非常详细地介绍了另一个晶格部分，最后是一个 [PWM 输出设备](http://hackaday.com/2015/12/16/taking-the-pulse-width-modulation-of-an-fpga/)。虽然各部分略有不同，但工作流程和原理是相同的。你只需要合适的 JTAG 加密狗来编程。