# 舒适体温计，配有令人印象深刻的 LED 显示屏

> 原文：<https://hackaday.com/2017/01/02/comfort-thermometer-with-impressive-led-display/>

对于学习使用 Arduino 板等微控制器的人来说，一个常见的早期项目是将温度传感器和 LCD 显示器连接起来，制作一个数字温度计。涉及的元件不多，但它为外设接口提供了方便实用的介绍。一旦你通过了技术教育的这一步，你还会回到温度计上来吗？可能不会，毕竟除了传感器和显示器，你还能给温度计增加什么呢？

如果你问过自己这个问题，也许你会对[理查德·史蒂文斯]的温度计项目感兴趣，他称之为[舒适温度计显示器](https://www.youtube.com/watch?v=9MXx4iAVi8o)。它采用 Ikea Ribba 框架的形式，内嵌 517 个 led，排列成一组中央七段显示屏、一圈条形图和一圈 RGB LEDs。幕后是大量的电缆和四个成型的条形板，以适应 led 周围的区域。显示屏循环显示温度、热指数和湿度的读数。

驱动这一切的是一对微控制器:用于 7 段的 ATMega328 和一系列控制条形图和 RGB LEDs 的 pic。另一个 PIC 处理与传感器的射频通信，这些传感器装在一个遥控盒中。我们在休息时嵌入了该设备的运行视频，我们相信你会同意这是一件令人印象深刻的作品。

 [https://www.youtube.com/embed/9MXx4iAVi8o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/9MXx4iAVi8o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



有一个强大的宜家黑客社区，他们用瑞典超市的产品创造出令人惊叹的东西。我们已经向你展示了[Richard]之前的一个项目，宜家灯里的气象站，但还有很多其他的项目，比如在宜家桌子上的数控机器 T2。