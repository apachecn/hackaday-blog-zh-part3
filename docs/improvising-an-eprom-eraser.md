# 临时制作一个 EPROM 橡皮擦

> 原文：<https://hackaday.com/2018/01/17/improvising-an-eprom-eraser/>

回到过去，当我们还在用磁化针拨弄比特时，改变 EPROM 上的数据并不像把它塞进编程器那么简单。这些存储芯片是用紫外光通过石英窗口照射到硅芯片上擦除的。当时，在出售的盒子里有整洁的小黑光灯来擦除这些芯片。现在已经不太需要这些芯片擦除器了，那么现在怎么对芯片进行擦除和编程呢？[使用在 70 年代曾风靡一时的组件制作自己的芯片橡皮擦](https://charlesouweland.wordpress.com/2017/12/28/improvising-an-eprom-programmer/)。

为了一个项目，他得到了一个旧的 2764 EPROM，但是这个芯片有一个问题——上面仍然有数据。幸运的是，旧电子产品具有很强的抗滥用能力，所以他拿出了显而易见的设备来擦除这个芯片，一个 300 瓦的晒黑灯。这几乎烧毁了房子，在灯下第二轮擦除六个小时后，仍然有未擦除的位。

在过去的 50 年里，我们产生紫外线的能力已经有了显著的提高，[查尔斯]记得他有各种各样的发光二极管，包括一些微小的 5mW 紫外线发光二极管。五毫瓦能做三百瓦做不到的事吗？有；发光二极管有合适的频率来翻转一点，擦除 EPROM 是强度和时间的函数。你真正需要做的只是将 LED 灯照射到芯片上几个小时。

擦除了这个老式芯片后，[查尔斯]用 ATMega 和台式电源拼凑了一个 EPROM 编程器，编程电压为 21V。它最终工作了，允许[查尔斯]的项目，一个老式的液晶显示器，使用老式的正确的部分有正确的数据。