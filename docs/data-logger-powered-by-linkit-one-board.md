# 由 Linkit One 板供电的数据记录器

> 原文：<https://hackaday.com/2015/10/02/data-logger-powered-by-linkit-one-board/>

[ 杰德·霍德森 ]组装了一个漂亮的小[数据记录器](https://www.prototypingcorner.me/projects/arduino/multi-channel-datalogger-with-oled-display/)，其核心是一个 Linkit One 板。它能够记录两个模拟通道和一个数字通道，还具有 PWM 功能。GPS 用于获得正确的时间，Freetronics 有机发光二极管显示器与一个屏蔽罩相结合，让用户可以实时查看数据。

数据以. CSV 文件的形式记录在 Linkit One 的内部存储器中，便于通过电子表格程序进行访问。LiPo 可充电电池保持电子流，一旦电量下降到 20%以下，系统就会发出警告。说到系统——[Linkit One](http://www.seeedstudio.com/depot/LinkIt-ONE-p-2017.html)板采用 ARM-7 处理器，并且具有适合 Arduino 屏蔽的接头。它面向可穿戴和物联网类型的设备。

如果你需要一个好的数据记录器，一定要看看这个项目。构建的所有代码和细节都可以在[Jed 的]博客上找到。