# intelloservo

> 原文：<https://hackaday.com/2016/04/22/intelliservo/>

伺服系统是用途极其广泛的致动器，广泛应用于需要受控机械运动的场合。驱动它们的通常方式是使用微控制器的 PWM 输出。但是如果你正在建造一个需要大量伺服系统的机器人或无人机，那么直接给伺服系统增加智能是有意义的。

[阿尔瓦罗·费伦·希福恩特斯]正是通过构建 [IntelliServo](https://hackaday.io/project/10071-intelliservo) 做到了这一点——这是一个插件，通过赋予常规伺服系统高端版本中的增强功能，使它们变得智能。与这个主题的其他观点相比，他的方法是不同的。IntelliServo 旨在取代任何常规伺服系统中的电子设备，并且不限于任何特定的品牌或类型。一旦升级，它可以读取伺服位置，温度和电流消耗。这允许有趣的用途，例如通过移动另一个伺服系统来控制一个伺服系统，或者通过监控伺服电流来检测碰撞或失速。多个伺服系统可以通过菊花链连接，由微控制器通过 I C 控制，或者直接由计算机通过 USB 控制。每块板都配有一个 [LPC11U24 32 位 Cortex-M0](https://developer.mbed.org/platforms/mbed-LPC11U24/) 微控制器、一个 [DRV8837](http://www.ti.com/product/DRV8837) 电机驱动器、一个 [TMP36](http://www.analog.com/en/products/analog-to-digital-converters/integrated-special-purpose-converters/integrated-temperature-sensors/tmp36.html) 温度传感器和一个 [PCA9508](http://www.nxp.com/products/interface-and-connectivity/interface-and-system-management/i2c/i2c-bus-repeaters-hubs-extenders/hot-swappable-level-translating-i2c-bus-repeater:PCA9508) I C 中继器。

该项目是开源的， [Github 库](https://github.com/bqlabs/IntelliServo)包含电路板设计、Arduino 库和示例、伺服固件和机械部件以及使用说明。这是一种模块化设计，允许使用外部控制器或通过板载微型 USB 插座直接运行。休息之后，请观看视频，了解 IntelliServo 的运行情况。

 [https://www.youtube.com/embed/W2uScJmLD4c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/W2uScJmLD4c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/FjYgxcrhwy4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FjYgxcrhwy4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

