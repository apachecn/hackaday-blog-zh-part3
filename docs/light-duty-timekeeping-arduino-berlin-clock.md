# 轻型计时:Arduino 柏林钟

> 原文：<https://hackaday.com/2015/12/01/light-duty-timekeeping-arduino-berlin-clock/>

就在我们以为已经看完了所有看时间的方法时， [[mr_fid]的柏林时钟出现了。它基于柏林参议院在 20 世纪 70 年代中期委托](http://www.instructables.com/id/Berlin-Clock-Arduino-Nano-DS1307-Real-Time-Clock-7/)[建造的真实时钟，于 1975 年竖立在著名的 Kurfürstendamm 大道上。20 年后，它退役并被移到历史悠久的欧罗巴中心外。](https://en.wikipedia.org/wiki/Mengenlehreuhr)

这个时钟使用集合论和 24 小时制来报时。从上到下:顶部闪烁的黄色圆圈表示过去的秒数；偶数秒开启，奇数秒关闭。两行红色方块是小时——最上面一行的每个方块代表五个小时，下面的每个方块代表一个小时。例如，在 11:00，将有两个顶部区块和一个底部区块被照亮。

下面两行显示了使用相同系统的分钟数。红色段表示 15、30 和 45 分钟，因此不需要计算超过几个 5 分钟的顶部段。和小时一样，底部一行表示每盏灯亮一分钟。

明白了吗？这是一个测验。现在几点了？看上面的图片，最上面一行有三段点亮。五个小时乘以三是 15:00，或者下午 3:00。下一排增加了两个小时，所以我们是下午 5:00。所有五分钟的片段都被点亮，这增加了 55 分钟。所以这张照片是在某个偶数秒的下午 5 点 55 分拍摄的。

最初的柏林钟饱受白炽灯泡寿命短的困扰。根据哪个灯泡熄灭，时钟可能会“关闭”少至一分钟，多至五个小时。[mr_fid]在这个美丽的建筑中保持了原汁原味，每个小时使用了两盏灯。这个复制品使用由 Arduino Nano 和实时时钟驱动的 led。由于 RTC 给出 0-23 范围内的小时和 0-59 范围内的分钟和秒钟，因此需要几个移位寄存器和一些模运算来转换成 set 理论时间。

[mr_fid]根据 QCAD 的设计，用胶合板和白橡木建造了围栏。圆角由橡木制成，第二个环由围绕喷雾罐弯曲的 3/8”胶合板条制成。休息过后，一个简短的时钟之旅正等着你。时间在浪费！

 [https://www.youtube.com/embed/SgrjEpEWO7k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/SgrjEpEWO7k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

