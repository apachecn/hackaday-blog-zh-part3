# 欺骗一个古老的协议来演奏曲子

> 原文：<https://hackaday.com/2015/11/06/tricking-an-ancient-protocol-to-play-tunes/>

2007 年实现了许多技术里程碑。例如，第一部 iPhone 于当年 1 月发布，同年晚些时候，新视野号飞越了木星。但即使取得了这些惊人的成就，沃尔沃仍然没有在他们的汽车音响系统上添加辅助输入。不过，他们的主机上确实有过时的端口，[卡勒]着手设计这个连接器来容纳辅助输入。

问题中的连接器是后面的一个 8 针 DIN，在过去的日子里(大约八年前)会被用于 CD 换碟机。由于 CD 现在已经是旧闻了，[卡勒]利用这一特性进行了黑客攻击。第一个障碍是 CD 换碟机不能从菜单中选择，除非主机确认那里有什么东西。[卡勒]使用 Arduino Nano 通过模拟 CD 换碟机使用的协议来欺骗主机。从那里，左和右音频引脚在同一个连接器被用来连接辅助电缆。

如果你有一辆像[卡勒]这样没有 aux 输入的近乎古董的沃尔沃，并且你想尝试这样的东西，Arduino 的源代码可以在项目页面上找到。当然，如果你没有沃尔沃，有很多其他方法可以将辅助输入接入其他各种设备，比如 80 年代的音箱或者 T2 普通 CD 播放器上的带状电缆。然而，事情并不总是一帆风顺，所以也有一些非标准选项。