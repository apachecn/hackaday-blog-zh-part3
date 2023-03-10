# 闪烁您的 ESP8266 有问题吗？认识一下 DIO 和 QIO

> 原文：<https://hackaday.com/2017/10/01/trouble-flashing-your-esp8266-meet-dio-and-qio/>

[【Pete】正在使用基于古老的 ESP8266 的 WEMOS 板建造一个热水浴缸控制器。](https://tech.scargill.net/a-flashing-esp-chips-surprise/)组装完成后，将电路板插入 USB,【Pete】按下闪光灯按钮。没有骰子。对某些终端软件的调查显示校验和错误。

假设这块板子死了，[皮特]抓了另一块——也遇到了同样的问题。WEMOS 板不会编程，但其他板没有问题。感觉到可能有些不对劲，进一步的研究是有序的。出现了一个讨论 ESP8266 不同编程模式的论坛帖子。

事实证明，ESP8266 使用不同类型的闪存，对于给定的硬件设置，必须选择正确的编程模式。这些模式被称为 DIO 和 QIO，分别表示“双 IO”和“四 IO”。这是指用于与闪存对话的 IO 线数量。还有其他模式，称为 DOUT 和 QOUT。通过查看数据手册，确定片上闪存芯片支持的模式非常重要。显然，这在一些预构建的模块上可能很困难，所以实验是这里的关键。

如果选择了错误的模式，写入闪存将会失败，回读将会出现校验和错误。很简单，在 make 文件中更改一行，尝试不同的模式，看看哪一个有效。这个论坛帖子对这个问题有更深入的报道。

通过选择不同的闪存器件和 DIO 或 DOUT 模式，实际上也可以释放更多的 GPIO 引脚。当优化 ESP8266 设计以实现内存速度或最大 IO 灵活性时，这些知识非常有用。这是一个很好的教训，[查看数据手册](https://hackaday.com/2016/04/26/pillaging-the-wealth-of-information-in-a-datasheet/)以充分利用您的器件总是有好处的。