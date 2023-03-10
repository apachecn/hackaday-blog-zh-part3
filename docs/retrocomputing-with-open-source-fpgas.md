# 使用开源 FPGAs 进行逆向计算

> 原文：<https://hackaday.com/2017/08/28/retrocomputing-with-open-source-fpgas/>

几年前，我们看到了 Lattice iCE40 比特流的逆向工程，打开了 FPGAs 完全开源开发工具链的大门。这是来自[Clifford Wolf]、[Mathias Lasser]和[Cotton Seed]的数量惊人的工作，但是从那以后我们就没有看到“冰风暴计划”的全部内容。现在，这种情况即将改变，而且是以最酷的方式。[【猪仔】正在 ICE40 开发板](https://forum.mystorm.uk/t/acorn-atom-implementation-for-mystorm-blackice/228)上逆向计算。

这是 Acorn Atom 在 myStorm BlackIce 板上的实现。该板基本上只是一个 Lattice iCE40 FPGA、一些支持元件和一堆引脚接头，其中一些位于不太方便的 Arduino 引脚排列中。通过将一些 Acorn Atom 实现和一个 6502 内核移植到 verilog 上，[hoglet]能够将一台很酷的老式逆向计算机装到开源 FPGA 开发板上。视频输出通过电阻 DAC 驱动 VGA 电缆，键盘输入通过 PS/2。

关于 Acorn 的开源实现的几乎所有东西都是有效的，在 iCE40 FPGA 中还有很多东西。[hoglet]能够以 25MHz 运行 6502 内核，这意味着几乎每个基于 6502 的系统都应该能够在 BlackIce 板上运行。