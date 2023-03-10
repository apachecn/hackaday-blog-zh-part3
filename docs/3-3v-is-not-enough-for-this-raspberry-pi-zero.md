# 3.3V 不够这个树莓 Pi 零

> 原文：<https://hackaday.com/2016/08/14/3-3v-is-not-enough-for-this-raspberry-pi-zero/>

Raspberry Pi Zero 的价格和尺寸非常适合集成到您的项目中。除非，你的项目涉及到很多 5 V 设备。那就只求被炸了。

[大卫·布朗] [通过用电平转换器断开引脚解决了这个问题](https://hackaday.io/project/11222-raspberry-pi-zero-breakout)。他使用扁平柔性电缆和一些引脚头。同时，他增加了一个全尺寸的 USB 端口和电源接头。(通过弹簧针将 USB 连接到主板会获得额外的 hack 点数。)

该板现已进入第三版，牺牲了一个 Pi 零点，并了解了为何许多板在 2.0 版中包含过压保护。对于 Pi 与非 3.3 V 世界的接口问题，这是一个干净利落的解决方案。

当它还是新的时候，我们看到了很多圆周率为零的附加元件。毫无疑问，这一部分是由于我们的[圆周率零点竞赛](https://hackaday.io/contest/9326-adafruit-pi-zero-contest)，但我们打赌这也是由需求驱动的:需要 [VGA 输出](http://hackaday.com/2016/02/21/5-vga-for-raspberry-pi/)，或者[四轴飞行器控制](http://hackaday.com/2016/02/16/a-quadcopter-controlled-by-a-pi-zero/)，或者仅仅是[点亮耗电的 led](http://hackaday.com/2016/02/14/controlling-rgb-leds-with-the-pi-zero/)。你的圆周率只有在你创造它的时候才是万能的。