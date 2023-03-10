# 完美风暴:开放式 ARM + FPGA 板

> 原文：<https://hackaday.com/2016/08/03/the-perfect-storm-open-arm-fpga-board/>

在过去，摆弄 FPGAs 是一件令人望而生畏的事情。您必须支付大约 100 美元来购买开发工具包，签署魔鬼协议来获得工具链，只有这样，您才能开始学习。在过去的几年里，许多力量汇聚起来，将 FPGA 体验带到了即使是最廉价、最有原则的开源黑客也能达到的范围内。

[Ken Boak]和[Alan Wood]组装了一个真正的 FPGA 板,目标是让价格低于 30 美元。他们基本上采用了一个 Lattice iCE40HX4K、一个 STMF103 ARM Cortex-M3 微控制器和一些 SRAM，并将其全部放在一块板上。

Lattice 部分是一个自然的选择，因为 [IceStorm 项目](http://www.clifford.at/icestorm/)为它创建了一个完全开源的工具链。(观看【Clifford Wolf】的[演示](http://hackaday.com/2015/12/29/32c3-a-free-and-open-source-verilog-to-bitstream-flow-for-ice40-fpgas/))。ARM 芯片用于在启动时将比特流加载到 FPGA 中，并提供 USB 连接、ADC 引脚和其他外设。板上有足够的 RAM 来完成很多工作，在 ARM 和 FPGA 之间，GPIO 引脚数不清。

建模一个开放的处理器内核？当然可以。高速数字信号捕获？为什么不呢？它甚至连接到一个树莓派，所以你可以使用整个事件作为一个高速外设。有了这么多的灵活性，你几乎没有什么是不能做的。诀窍是驯服野兽。这就是你的切入点。