# 拼凑一个连环背包

> 原文：<https://hackaday.com/2017/01/30/hacking-together-a-serial-backpack/>

串行背包实际上只不过是一个屏幕和一些微控制器胶水来驱动它。锤子只不过是棍子末端的硬化重物。但是当你面对一个钉子，或者一个输出一系列诊断数据的设备时，没有什么比拥有合适的工具更好的了。

[![1383501485329153153](img/c41958975acb45153df7d5b419c7e45f.png)](https://hackaday.com/wp-content/uploads/2017/01/1383501485329153153.jpg) 【奥格丹托】[利用手头的零件和一些很棒的旧代码的移植，打造了自己的系列背包](https://hackaday.io/project/19572-lcd117e-adapted-for-a-nokia-1100-display)。切开一个诺基亚 1100 图形显示器，从零件抽屉里拿出一张 PIC，他得到了他需要的硬件，他在[Peter Andersen]的[普通字符 LCD 库](http://www.wulfden.org/TheShoppe/k107/pha/pha.shtml)和[spiralbrain]的[诺基亚 1100 图形 LCD 库](https://web.archive.org/web/20120102020033/http://www.sunbizhosting.com/~spiral/1100/)中找到了他的代码的良好开端。[ogdento]增加了对背光的控制，将两个软件融合在一起，瞧！

一个简单的带有串口的屏幕是一个很好的设备，它是一个很好的项目。当然，在 T1 之前，我们已经在这里见过他们了。既然你*可以*在网上订购一个，为什么不自己做一个呢？谁知道在这个过程中你会想出什么样的疯狂定制。