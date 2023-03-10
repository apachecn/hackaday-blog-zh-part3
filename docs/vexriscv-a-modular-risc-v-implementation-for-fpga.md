# VexRiscv:一种面向 FPGA 的模块化 RISC-V 实现

> 原文：<https://hackaday.com/2017/07/21/vexriscv-a-modular-risc-v-implementation-for-fpga/>

由于 FPGA 只是芯片上数字逻辑元件的海洋，因此使用至少部分 FPGA 电路来构建 CPU 并不罕见。VexRiscv 是使用一种叫做 SpinalHDL 的语言实现的 [RISC-V CPU](https://github.com/SpinalHDL/VexRiscv) 架构。

SpinalHDL 是一种高级语言，概念上类似于 Verilog 或 VHDL，可以编译成 Verilog 或 VHDL，所以应该可以兼容大多数工具链。VexRiscv 在这个项目中表现很好，因为它是非常模块化的。您可以添加指令、MMU、JTAG 调试、缓存等等。

当你在 FPGA 中构建一个 CPU 的时候，你一般要做三个选择中的一个。你可以自己开发，这很有趣，但需要在设计和相关工具上做很多工作，例如交叉编译器或操作系统。你可以“借用”一个现有的架构或设计，它可能合法也可能不合法，这取决于你的选择。您也可以使用商业产品。虽然其中一些在某些情况下是免费的，但你需要为任何实质性的东西付费。

这种开放式实现为您提供了一种利用一些优秀工具的简单方法。有一个 GDB 的调试接口和一个自由操作系统端口。即使开启所有特性，32 位器件也能实现 1.16 Dhrystone MIPS/MHz。这与商用 32 位处理器不相上下。

文档也很好。您可以在 Linux 系统上模拟 CPU。还有一些常见 FPGAs 的实现编号。例如，Cyclone V 芯片可以支持 115 MHz 至 187 MHz，具体取决于选项。即使是 Cyclone II 也可以运行 156 MHz 的基本版本或 92 MHz 的精心设计版本。

甚至还有一个完整的片上系统设计作为例子。老实说，着手这样一个定制项目不会是一个半小时的项目。但是有了提供的文档，您可以学到很多东西，或者在 FPGA 中部署一个重要的处理器方面有一个很好的开端。甚至还有一个添加全新指令模块的例子。

我们之前已经讨论过引导一个全新的 CPU 的困难。有了 VexRiscv，你就不用担心这个了。当然，如果你想事事亲力亲为，这里有[的一些灵感](https://hackaday.com/2017/01/13/fpga-computer-covers-a-to-z/)。