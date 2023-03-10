# 会弄坏你电脑的 USB Type-C 线

> 原文：<https://hackaday.com/2016/02/04/the-usb-type-c-cable-that-will-break-your-computer/>

大约从 1997 年开始，USB 就出现在我们的台式机和笔记本电脑上，从那时起，它就一直是计算机外设的支柱。对于连接鼠标、键盘、网络摄像头、微控制器开发板和其他任何东西来说，没有其他连接器像它一样有用；它甚至是手机的标准电源连接器。USB 实现者论坛的最新进展是 USB Type-C 连接器，这是一种具有千兆带宽的设备，可以处理足够为笔记本电脑供电的电流。这是未来，即使苹果的单端口奇迹不是。

![Ground is red, V is Black. Photo: Benson Leung](img/77ddd0c6d2c569e6f5db5d29af22ad12.png)

Ground is red, V is black. Photo: [Benson Leung](https://plus.google.com/+BensonLeung/posts/EBGMagC46fN?pid=6246825014916118210&oid=102617628172847077584&authkey=CLb9xZv-vuygTw)

默认情况下，未来的电缆是新的。这意味着制造商仍在计算端口，以及如何连接它。你可能认为记住“红色=电源，黑色=接地”很容易，但是一些制造商犯了严重的错误。

[Benson Leung]是一名谷歌工程师，负责 Chromebook Pixel 产品，是 USB Type-C 连接器的大力支持者，也是亚马逊上 USB Type-C 连接器的一名非常多产的评论者。他测试的最新电缆摧毁了他的测试设备，包括一台 1500 美元的 Chromebook Pixel 2 (链接失效，试试[互联网档案馆](https://web.archive.org/web/20170203022724/https://plus.google.com/+BensonLeung/posts/HzkGqnWcyYM))。一根电缆是如何做到这一点的？制造商调换了黑色和红色。

有问题的电缆[是一根 SurjTech 3M 电缆](https://plus.google.com/+BensonLeung/posts/EBGMagC46fN),幸好已经从亚马逊上取下。交换 GND 和 Vbus 并不是唯一的问题——超高速线不见了，这意味着这实际上只是一条带有 C 型连接器的 USB 2 电缆。USB 规范要求的电阻是错误的值，被配置为下拉电阻而不是上拉电阻。

这不是电缆不符合设计规格的问题。以太网电缆，特别是 Cat6 电缆，[已经被证明可以在*工作*，但是不符合 Cat6 电缆](http://hackaday.com/2016/01/30/is-your-cat-6-ethernet-cable-cat-6-probably-not/)的规格。那是见不得人的制造，但不会坏电脑。这是计算机电缆世界的新低，但至少这种电缆已经从亚马逊消失了。