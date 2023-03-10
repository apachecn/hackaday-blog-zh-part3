# 32 C3:ice 40 FPGA 的免费开源 Verilog-to-Bitstream 流

> 原文：<https://hackaday.com/2015/12/29/32c3-a-free-and-open-source-verilog-to-bitstream-flow-for-ice40-fpgas/>

[Clifford]展示了一个用于 FPGAs 编程的[完全开源的工具链](https://media.ccc.de/v/32c3-7139-a_free_and_open_source_verilog-to-bitstream_flow_for_ice40_fpgas#video)。如果你不认为这是一件令人印象深刻的作品，你就没有真正理解 FPGAs。

这个工具链，或者 FPGA 孩子们喜欢称之为“流”，由三个部分组成:Project IceStorm，一个可以构建在 FPGA 内部翻转单个位的位流的低级工具，阿拉克尼-pnr，一个将符号网表转化为 IceStorm 需要的物理东西的布局布线工具，以及 Yosys，它将 Verilog 代码合成为阿拉克尼需要的网表。[Clifford]开发了 IceStorm 和 Yosys，所以他知道他在说什么。

最令人印象深刻的是，FPGAs 并不是这种流动的唯一目标。因为它都是开源的和可修改的，它也被用于设计定制的 ASICs，当你需要自己的定制芯片时，知道这一点很好。[Clifford]在 Yosys 中的主要关注点是形式验证——确保 FPGA 的行为符合 Verilog 代码的预期。一个完全开源的工具链使得这项工作成为可能。

如果你一直在关注[Al Williams]的 FPGA 帖子，无论是[这个介绍](http://hackaday.com/2015/08/19/learning-verilog-on-a-25-fpga-part-i/)还是他最近的[中级系列](http://hackaday.com/2015/12/16/taking-the-pulse-width-modulation-of-an-fpga/)也是基于相对便宜的 Lattice iCEStick 开发套件，这个视频都是必看的。这是对免费 FPGA 工具前沿的精彩介绍。