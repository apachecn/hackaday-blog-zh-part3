# FTDI FT232R 中的硅缺陷，以及一个整洁的 RF VCO 项目

> 原文：<https://hackaday.com/2018/06/15/silicon-bugs-in-the-ftdi-ft232r-and-a-tidy-rf-vco-project/>

[Scott Harden]来信告诉我们，他使用 FT232 芯片直接从笔记本电脑向 AD98850 数字信号发生器发送 SPI，取得了一些成功。至少那是他的目的地。但正如生活中经常发生的那样，超过一半的乐趣是到达那里，找到一些仍未解决的硅错误，并(在简单地将芯片换成一个有效的芯片后)用热胶将其封装，放入一个漂亮的盒子，然后放在架子上。

原则上，FTDI FT232 系列芯片具有 bit-bang 模式，允许您从目标计算机上的一个相当简单的 API 控制各个引脚，使用它们的驱动程序，并且基本上不需要在任何平台上安装任何东西。[我们早在 2009 年就写了这个功能](https://hackaday.com/2009/09/22/introduction-to-ftdi-bitbang-mode/)，【Scott】问自己为什么没有看到更多的黑客利用 bit-bang 模式。

[![](img/788f825d436f6486be28f3630def84af.png)](https://hackaday.com/wp-content/uploads/2018/06/232r-scope2-640x427.jpg)

“Square” waves

然后他艰难地回答了自己的问题，花了几个小时“调试”他的代码，直到他偶然发现了 [FTDI 勘误表注释](http://www.ftdichip.com/Support/Documents/TechnicalNotes/TN_120_FT232R%20Errata%20Technical%20Note.pdf) (PDF)，其中他们承认 bit-bang 模式在 FT232R 和 FT232RL 器件上根本没有获得正确的时序。FTDI 声称他们在随后的芯片版本中修复了这个错误，[，但是社区还没有能够证实它。如果你想使用非常酷的 bit-bang 模式，请避开 FT232R 芯片，这种芯片出现在一直流行的 FTDI 电缆和许多适配器软件狗中。](http://blog.bitheap.net/2012/03/ft232r-bitbang-mode-is-broken.html)

这里的好消息是双重的。首先，现在你知道了。其次，bit-bang 模式非常有用，可以与厂商的其他芯片配合使用。特别是 FT232H 和 [FT230X 芯片工作正常](https://stb-tester.com/blog/2016/05/26/ir-post-mortem)、[等等](https://www.intra2net.com/en/developer/libftdi/)。[Scott]启动并运行了他的命令行控制数字 VCO。结局好就一切都好？

最后，我们将在评论区提问。其他制造商的廉价 USB 串行芯片是否具有易于访问的 bit-bang 模式？你们有人在用 USB bit-bang 吗？如果有，是为了什么？