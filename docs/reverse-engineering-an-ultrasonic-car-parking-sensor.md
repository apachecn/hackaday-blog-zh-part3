# 逆向工程超声波汽车泊车传感器

> 原文：<https://hackaday.com/2017/05/16/reverse-engineering-an-ultrasonic-car-parking-sensor/>

它已经成为一种常见的景象，现代汽车上的必备功能，一排嵌入后保险杠的超声波传感器。它们是停车传感器的一部分，是对那些深度知觉有点像彩票的司机的一种帮助。

[Haris Andrianakis]更换了 hs 汽车上的传感器系统，并对他拆除的那个系统产生了足够的兴趣[对其进行逆向工程并探测其工作方式](http://www.candrian.gr/index.php/reverse-engineering-car-parking-sensors/)。他发现了一组令人惊讶的简单组件，一个 Atmel 处理器，一组 CMOS 逻辑芯片和一个运算放大器。压电传感器兼作扬声器和麦克风，CMOS 模拟开关交替传递超声波脉冲和接收响应。处理器向看门狗电路发送一个信号音，当处理器崩溃且信号音停止时，看门狗电路触发复位。不幸的是，他没有深入研究接收器前端电路，但我们可以从图片中看到，它涉及一个带有一组可变电感的 LC 滤波器。

如果你曾经对这些系统感兴趣，这篇文章是一篇有趣的读物。如果你想要更多的超声波雷达，看看这个[扫频显示项目](http://hackaday.com/2014/12/22/green-sweep-for-your-ultrasonic-rangefinder/)，或者这个[超声波虚拟触摸屏](http://hackaday.com/2014/08/24/a-virtual-touchscreen-3d-ultrasonic-radar/)。