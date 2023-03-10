# 没有为 FPGAs 做好准备？试试 CPLD

> 原文：<https://hackaday.com/2015/12/19/not-ready-for-fpgas-try-a-cpld/>

[Kodera2t]想试验可编程逻辑。他没有使用 FPGA 板，而是决定构建自己的 [CPLD(复杂可编程逻辑器件)板](https://hackaday.io/project/8754-very-simple-cpld-trainer)，内置编程器。CPLD 是 Xilinx 9536，价格低廉，虽然已经过时，但仍然很容易获得。该板的程序员使用 FT232RL，总成本非常低([kodera2t]称其价格在树莓 Pi 零或约 4 美元的范围内)。

从用户的角度来看，CPLD 只是一个小 FPGA。从内部来看，它们实现您的设计的方式有很大的不同。尽管不同的产品系列之间存在差异，但 CPLDs 通常使用大量的逻辑门，排列成 AND/OR 链。通过将输入和反相输入输入到“与”门，然后对结果进行“或”运算，可以构建有趣的逻辑电路。然而，现代 CPLDs 使用 Verilog 或 VHDL，所以你可以像使用 FPGA 一样描述你想要的东西，软件会计算出如何使用底层电路来提供你想要的东西。

FPGAs 通常使用不同的方法来表示逻辑，通常是 LUT 或相当于真值表的查找表，从一组输入中定义输出。然而，也存在其他 FGPA 架构(如基于多路复用器的 FPGAs)。FPGAs 通常比 CPLD 具有更灵活的互连。然而，从实际的角度来看，你可以把 CPLD 看作一个“小”FPGA。CPLDs 几乎总是在非易失性存储器中保存自己的配置，所以它们会立即出现；只有少数 FPGAs 能做到这一点。

Hackaday.io 上的[kodera2]项目有非常全面的编程说明，也有电路板的 PCB 布局。4 美元的价位很难被打破，但是一个更强大的 FPGA 板不需要比这个价格贵太多。然而，如果您想要从 PCB 开始构建一切的体验，CPLD 项目可以让您以较小的投资启动并运行一些东西，而不必焊接超高密度的部件。另一方面，如果只是想学 Verilog 或者 VHDL，不需要任何硬件。[只需使用你的网络浏览器](http://hackaday.com/2015/07/21/learn-fpgas-in-your-browser/)。

下面有一个简短的视频。

 [https://www.youtube.com/embed/K1VeIDKLIHw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/K1VeIDKLIHw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

