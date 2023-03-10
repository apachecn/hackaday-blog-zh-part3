# 英特尔 8085 微处理器训练器

> 原文：<https://hackaday.com/2017/01/15/an-intel-8085-microprocessor-trainer/>

英特尔 8085 微处理器早在 40 年前就推出了，与其同时代的 Z80 和 6502 一样，在微处理器历史上几乎是一只恐龙。但这并不能阻止它仍然被包括在世界上许多地方的计算机工程学生的教学大纲中。为什么 40 岁的微处理器仍然出现在计算机体系结构教科书中，而不是计算机历史中，这有点令人费解。但是，有一整个行业因大学实验室和学生需要“8085 微处理器培训套件”而蓬勃发展。[TisteAndii]刚在尼日利亚读完大学，那里的这些设备不是本地制造的，需要进口，通常价格超过 100 美元。

这就是为什么他最后一年的项目是一个低成本的英特尔 8085 微处理器训练器。这是一个极简设计，有一些基本的读/写内存、程序执行和寄存器检查，还没有提供单步执行或中断。监控程序没有加载到 EEPROM 中。相反，使用 PIC18 并连接到 8085 地址、数据和控制引脚。这使得用 C 编写监控程序比用汇编语言更容易。并允许使用带 SPI 接口的 1.8 英寸 LCD，而不是用于这类套件的更常见的 7 段显示器。[TisteAndii]构建了一个 6×4 的输入键盘，但无法解决去抖问题，最终采用了 5×4 的薄膜键盘。

作为一名新手，他最终在他的[电路板布局](https://github.com/brianrho/Rho85/tree/master/CAD)中发现了一个重大缺陷——他没有将 SRAM 和 PPI 设备连接到数据总线。一堆跳转链接似乎解决了这个问题，但它并不完美。这一点，以及其他一些问题给了他很大的悲痛，但接近尾声时，这一切都起作用了，几乎。最重要的是，他的 BoM 成本约为 35 美元，这使得它比尼日利亚的商业单位便宜得多。

虽然一些黑客可能认为这是一个微不足道的项目，但它解决了一个局部问题，我们希望设计的下一次迭代能够改进该工具包，使其更易于使用。