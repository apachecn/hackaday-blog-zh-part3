# 带 ATtiny85 的 DIY I2C 设备

> 原文：<https://hackaday.com/2016/11/07/diy-i2c-devices-with-attiny85/>

[Pawel]有一个气象站，它的神经中枢是树莓皮。他[想要包括一个光传感器](https://quadmeup.com/attiny85-light-sensor-i2c-slave-device/)，但问题是，Pi 没有内置的 ADC 来读取光敏电阻的电压，他(大概)在他的垃圾箱里有这个光敏电阻。当然，你可以购买 I2C 的 ADC 芯片和模块，但当你已经有一个片上带 ADC 外设的微控制器时，为什么还要这么麻烦呢？

[Pawel]连接了一个非常简单的电路，下载了一些 I2C 从模式代码，并添加了一个 LED 灯。如果你感兴趣，这些都在 GitHub 上。

[![cropped_shot_2016-10-21-112958](img/3093ad8ddaf4c5b01baba8ced080e38a.png)](https://hackaday.com/wp-content/uploads/2016/10/cropped_shot_2016-10-21-112958.png)

Bright by Day, Dark by Night!

我们报道这个是因为我们很少看到有人为 I2C 从属设备编码。每个人和他们的妈妈*都使用* I2C 来连接传感器，对于这一点，Pi 上的 Arduino“Wire”库或“i2c-tools”做得很好。但是当你想让*生产*I2C 设备时，你会怎么做呢？[Pawel]的项目使用了 [TinyWireS](https://github.com/rambo/TinyWire/tree/master/TinyWireS) ，一个用于 AVR ATtiny Arduino 项目的从模式 SPI 和 I2C 库。

在这里，[Pawel]只是想要一个光传感器。但是如果你正在建造你自己的设备，天空是无限的。你能想到的最深奥的 I2C 传感器是什么？(自 2010 年以来，我们真的没有见过 I2C 从属设备被黑[吗？)](http://hackaday.com/2010/08/06/make-your-own-mindstorm-sensors/)