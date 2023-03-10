# 最小的控制板适合 N 轨距火车模型

> 原文：<https://hackaday.com/2017/06/27/tiniest-control-board-fits-inside-an-n-gauge-model-train/>

[kodera2t]发现了 VL53L0X 飞行时间传感器，并认为[这将是一种无需触摸即可控制模型火车](https://hackaday.io/project/25622-very-tiny-motor-driver-with-time-of-flight-sensor)运行的伟大方式。在演示视频中，他用自己的话[解释道。](https://www.youtube.com/watch?v=5pgxKt1Id9o)

该传感器对于 N 轨距的火车来说足够小，相当于 1:148 的比例，或者轨道之间大约 9 毫米。他的想法是建造一个可以安装在机车内部的微型控制板:10 毫米乘 40 毫米。他的开发板由 ToF 传感器、ATMega328P-MMH、USB 串行接口和德州仪器 DRV8830 电机驱动器组成。他通过轨道上的 6V 电源给电路板供电。

现在[kodera2t]正在使用 ToF 作为一种手势控制器，让火车开始滚动，但人们可以想象传感器可以被集成到更高级的程序中，比如根据桥的高度，让火车在直道上加速，在弯道上减速。

我们在 Hackaday 上公布了一堆【kodera2t】的微型电路板项目，包括[最小的基本计算机](http://hackaday.com/2016/07/08/smallest-basic-computer/)，他的[最小频率计数器](http://hackaday.com/2016/07/02/hackaday-prize-entry-a-minimal-attiny-voltage-and-frequency-counter/)，他的 [VFD 放大器。](http://hackaday.com/2016/09/24/now-is-the-golden-age-of-artisanal-non-traditional-tube-amps/)

 [https://www.youtube.com/embed/5pgxKt1Id9o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5pgxKt1Id9o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

