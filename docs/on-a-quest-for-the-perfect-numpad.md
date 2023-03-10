# 寻找完美的数字小键盘

> 原文：<https://hackaday.com/2018/03/12/on-a-quest-for-the-perfect-numpad/>

很多时候，在一个设备中得到你想要的东西的唯一方法就是自己动手制作。嗯，也许不是唯一的方式，但我们都肯定地告诉自己，这是唯一的方式，这可能是真的。我们不知道【奥拉夫·瓦特内】对[构建他自己的蓝牙机械数字键盘](http://equalpasta.com/2017/10/29/making-a-bluetooth-numpad-part-1-soldering-and-parts/)的 DIY 迫切感是真实的还是自我强加的，但无论如何，我们很高兴他记录了这个过程以供我们观看。

[![](img/27c294902f02aa43e9fa247669cf22bd.png)](https://hackaday.com/wp-content/uploads/2018/03/btkbd_detail.jpg) 在他的博客上分成三个独立的帖子，他的定制数字小键盘的建造从从全球速卖通购买一套设备开始，这是足够天真的。在一个相当奇怪的转折中，套件抵达*组装*，这导致了一段艰苦的拆焊期，以分离所有最初想要的主要部件【Olav】。节省时间到此为止。

一旦他从工具箱的印刷电路板上取出所有的机械钥匙，他就去镇上手动布线矩阵。在测试以确保所有按键都正确接线后，matrix 连接到了一个[Adafruit Feather 32u 4 blue fruit](https://learn.adafruit.com/adafruit-feather-32u4-bluefruit-le/overview)。随着电子产品的分类，[Olav]转移到软件方面。在这里，他能够实现他的主要目标之一，拥有一个既能通过 USB *又能通过*蓝牙工作的数字小键盘。

流程的最后一步是[制作木制外壳](http://equalpasta.com/2017/11/24/making-a-bluetooth-numpad-part-3-enclosure/)。它基本上就像一个相框，要特别注意确保外壳上有适当的开口，以便开关和 USB 端口可以穿过，而不会破坏设备的整体外观。

多亏了廉价的支持 USB 的微控制器，手工制作的工匠键盘现在已经成为现实。这个项目是一个开始定制输入设备的好方法，并且[它只会从这里变得更好](https://hackaday.com/2017/11/10/an-awesome-open-mechanical-keyboard/)。