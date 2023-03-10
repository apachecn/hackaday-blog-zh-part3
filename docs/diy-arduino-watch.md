# DIY Arduino 手表

> 原文：<https://hackaday.com/2016/04/21/diy-arduino-watch/>

我们最初认为[Alexis Ospitia]的手表是用 Arduino 制造的运动手表，但它实际上是用 Arduino 制造的[运动手表。这解释了手表告诉你当前温度和湿度的奇怪能力。](http://www.instructables.com/id/Arduino-Watch-Sport/?ALLSTEPS)

手表的核心是一个 Arduino Mini。为了更好地报时，增加了一个实时时钟模块。一个 [DHT11](http://hackaday.com/2012/01/11/dht11-humidity-and-temperature-sensor-package/) 监控温度和湿度。充电电路和锂电池提供电力。最后，手表通过诺基亚 5110 的 LCD 显示日期、时间和其他数据。我们可以告诉你最后一部分会中断。

就算你觉得手表有点矮胖，教程也很华而不实。[Alexis]不厌其烦地单独绘制并描述了腕表结构的各个部分。他解释了每一个管脚，它们的作用，并提供了一张 Arduino 电线的烧结图。提供了代码；要对手表进行编程，必须使用 USB 转串行模块。

对于外壳，他用薄铝板做了一个盒子，并在组件上绑上了皮带。最终的结构看起来很酷，有一种技术朋克的风格，而且相当紧凑。甚至可以说是运动型的。