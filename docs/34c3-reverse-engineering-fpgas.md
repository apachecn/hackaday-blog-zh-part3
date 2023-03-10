# 34C3:逆向工程 FPGAs

> 原文：<https://hackaday.com/2018/01/17/34c3-reverse-engineering-fpgas/>

我们曾经认识一个人，他曾经告诉我们，他第一次坐飞机的时候，他是从飞机上跳下来的。这是他走下飞机前的第十一次飞行。[马蒂亚斯·拉塞尔]也有类似的故事。尽管他是几年前解码 iCE40 比特流格式的两人中的一员，但他在他的 34C3 演讲中承认，他从未学会如何使用 FPGAs。他的演讲涵盖了他如何对 iCE40 和 Xilinx 7 系列设备进行逆向工程。

如果你在 Verilog 和 VHDL 方面习惯了 FPGAs，[Mathias]将向你展示一个全新的行、列和平铺视图。即使你从来没有打算在那个层次上工作，有时理解底层的硬件也会激发一些在抽象层次上更难获得的洞察力。

理论上，逆向工程应该没那么难。该设备具有一定量的资源，并且比特流识别这些资源如何连接在一起，并且可能对一些查找表进行编程。但是在实践中，这很困难，因为实际上没有文档，包括您需要了解的资源的详细信息。

例如，在视频中，你可以看到 Lattice 的逻辑单元图。有几个选项可以做一些事情，比如绕过触发器、设置查找表等等。有许多选项可用于设置该配置，但这甚至没有解决如何将输入和输出连接到路由资源的问题。

当然，你知道他管理了 iCE40 解码，因为他和[Clifford Wolf]做了[开源网格工具链](https://hackaday.com/2015/05/29/an-open-source-toolchain-for-ice40-fpgas/)背后的工作。我们甚至在我们的几个 [FPGA 教程](https://hackaday.com/2015/12/17/pwm-on-the-lattice-icestick/)中使用了这个工具链。

[https://media.ccc.de/v/34c3-9237-reverse_engineering_fpgas/oembed](https://media.ccc.de/v/34c3-9237-reverse_engineering_fpgas/oembed)