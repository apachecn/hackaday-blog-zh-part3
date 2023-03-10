# 这个世界需要 FPGA Arduino 吗？

> 原文：<https://hackaday.com/2016/03/09/does-the-world-need-an-fpga-arduino/>

把 FPGA 和 Arduino 混在一起会得到什么？输出引脚太少的 FPGA 开发板？还是无法编程的 Arduino 形式的电路板？

幸运的是，ICEZUM Alhambra 看起来避免了这些陷阱，至少在大部分情况下。它基于 Lattice iCE40 FPGA，我们之前已经[讨论过多次](http://hackaday.com/2015/05/29/an-open-source-toolchain-for-ice40-fpgas/)，因为它的[廉价开发板和开源开发流程](http://hackaday.com/2015/08/19/learning-verilog-on-a-25-fpga-part-i/)。事实上，当 BQ 们[在为 FPGA 家族](http://hackaday.com/2016/02/23/icestudio-an-open-source-graphical-fgpa-tool/)开发一个易于使用的 GUI 时，我们想知道他们在忙些什么。现在我们知道了——它是 FPGA“Arduino”的支持软件。

[![Icezum-rev1-1607-img1-peq_thumbnail](img/f77984b70a9fb2a91dc141370809d3c5.png)](https://hackaday.com/wp-content/uploads/2016/03/icezum-rev1-1607-img1-peq_thumbnail.png)

Alhambra 板本身看起来与 Arduino 兼容，在左侧的行和所有行之间有可怕的间隙，所以它将与您现有的护盾一起工作。但他们也在更便于黑客使用的布局中将引脚加倍:SVG——信号、电压、接地。这非常适合使用三线电缆连接小型有源传感器，就像您用于伺服系统的那种电缆一样。(Hackaday.io 有两个使用 SVG 引脚排列的 Arduino 克隆:分别是 [SMT](https://hackaday.io/project/2991-pipduino) 和 [DIP](https://hackaday.io/project/2080-gvsduino) 格式。)

iCE40 FPGA 有 144 个引脚，所以你可能会问自己它们都在哪里，坦率地说，我们也是。板上有八个用户 led，外加 28 个以引脚接头结束的 I/O 引脚。这使得大约 100 个潜在的 I/o 无法解释。在我们的书中，FPGAs 的主要吸引力之一是快速 I/o 的巨大可用性。尽管如此，它的 I/O 比普通的 Arduino 要多，所以我们不会抱怨太多。有时候简单是一种美德。一切都在 GitHub 上，但还没有移植到 KiCad，所以如果你有 Altium 的副本，你可以调整硬件。

我们已经看到 FPGA 项目如雨后春笋般涌现，随着[开源工具链使它们更容易获得](http://hackaday.com/2015/12/29/32c3-a-free-and-open-source-verilog-to-bitstream-flow-for-ice40-fpgas/)，我们想知道它们是否会成为主流；可重构硬件的诱惑如此之大。将 FPGA 放入 Arduino 兼容的外形中，并用开放的 GUI 支持它，这是一个有趣的想法。这个项目显然还处于非常早期的阶段，但我们已经迫不及待地想看看它将如何发展。如果有人拿到这些板子，告诉我们，好吗？

谢谢你的提示！