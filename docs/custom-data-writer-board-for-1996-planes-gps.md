# 1996 年飞机 GPS 的定制数据写入板

> 原文：<https://hackaday.com/2016/11/23/custom-data-writer-board-for-1996-planes-gps/>

[Dmitry Grinberg]最近购买了一架塞斯纳 150，其中包含一个 1996 年的旧 IFR 认证 GPS，KLN89B。GPS 装置包含一个数据库，根据法律，该数据库必须为 IFR 飞行保持最新。问题是，虽然霍尼韦尔仍然以电子形式提供数据，但[Dmitry]没有办法更新 GPS。最初的方法要么不再受支持，要么太贵，做起来很痛苦，要么由于他的 GPS 安装方式而不可用。

其中两种方法包括移除数据卡，它可以合法地从 GPS 的前面板滑出。数据卡是存储所有数据的东西，但它是一种专有卡，没有读卡器。因此，【Dmitry】的解决方案是[制作自己的读写器板](http://dmitry.gr/index.php?r=05.Projects&proj=21.%20KLN89)。

![Reading the card using the STM32F411 dev board](img/51671c651f015849d3e84b6161b60778.png)

Reading the card using the STM32F411 dev board

检查卡和他从易趣上买的另一个卡，他能够使用组件的数据表来计算卡连接器的引脚排列。从那里开始，他将其连接到 STM32 开发板，并证明他可以可靠地读取卡的内容。

完成后，他接下来围绕基于 5V [AT90USB646](http://www.atmel.com/devices/at90usb646.aspx) Atmel 8 位 AVR RISC 的微控制器设计了他的读写器板。板上还有一个 12V 升压转换器和一个用于插卡的连接器。

在制造他的电路板时，他将注意力转向了数据本身。霍尼韦尔仍然以 Windows EXE 文件的形式提供数字形式的更新数据。快速检查显示它包含一个 ZIP 文件，很快他就有了数据库本身。但事情没那么简单。大部分数据被加密了，通过更多的实验，他了解到数据应该在写入卡之前被解密。然而，[Dmitry]迎接了这一挑战，经过几天的努力，他发现加密相当简单，而且是基于从数据本身的密钥开始应用 CRCs。在剩下的麻烦的 8 个字节之后，他有了写入卡的正确的更新数据。

一旦他的制造板到达，他添加微控制器和其他组件，并让它读，写和擦除卡在任何时间。虽然他在自己的网站上提供了原理图和所有软件，但他也给出了大量免责声明，这是可以理解的，因为这是针对飞机上的 GPS。但是，即使你不需要使用它，你也会在他的网站上找到[Dmitry]关于这个项目的非常详细的报道。

![KLN89B GPS data card reader writer schematic](img/f57282596e9e2d472d3d16dff0ef9c85.png)

KLN89B GPS data card reader writer schematic

[Dmitry]在 Hackaday 也不陌生。他的项目范围很广，从用于 AVR 的加密 USB 引导程序到由播放完整歌曲的 CD 盒制成的 T2 贺卡，再到用环氧树脂封装的 T4 8×8 矩阵 LED 吊灯。