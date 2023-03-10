# 从 20 世纪 50 年代的万用表到互联网时钟

> 原文：<https://hackaday.com/2017/03/04/from-1950s-multimeter-to-internet-connected-clock/>

这些年来，我们在这里见过许多钟。有些是常规的，有些是深奥的。因此，在计时领域，我们并不经常看到新奇的东西。

严格来说，[Giulio Pons]的时钟项目一点也不新鲜。他从 20 世纪 50 年代拿了一个坏掉的万用表，在 Arduino Nano 和 ESP8266 模块的帮助下，[将其转换成一个时钟，在万用表的动圈表上显示时间](https://hackaday.io/project/20116-retrofitting-of-an-old-tester-from-1955)。他将万用表的前面板控制器连接到 Arduino 上来操作这个东西，并给它一个扬声器来播放警报声音。PIR 运动探测器激活时钟。在黑暗的时候，光敏电阻带来光明。时间通过互联网自动设置。[Giulio]之前试验了 RTC 模块，但发现网络连接使更改时间设置更容易。

这绝不是完美的时钟。例如，[Giulio]发现从 PWM 引脚驱动电表会产生不同的读数，这取决于灯等其他部件的 PSU 负载。但是时钟确实在工作，并且给这个原本可能是垃圾的地方注入了新的生命。

你们中那些记忆力好的人可能记得几年前的一个类似项目，该项目使用未经修改的万用表将时间显示为电压。当然，总有[频率计数器时钟](http://hackaday.com/2010/11/12/nixie-frequency-counter-gone-timepiece/)。