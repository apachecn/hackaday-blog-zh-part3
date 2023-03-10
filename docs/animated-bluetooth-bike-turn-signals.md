# 动画蓝牙自行车转向灯

> 原文：<https://hackaday.com/2018/05/24/animated-bluetooth-bike-turn-signals/>

厌倦了在多雨的温哥华骑自行车时每次都要用手示意转弯而冒着生命危险，[Simon Wong]决定他需要一些更高科技的东西。但是他决定把它变成他的第一个严肃的 Arduino 项目，而不是买现成的东西。考虑到最终的结果和一长串的功能，我们会说他真的把这个打得落花流水。如果这是他的开始，我们非常希望看到他从这里走向何方。

[![](img/1d8f0b85f99c505b3337b1eacf5e88b3.png)](https://hackaday.com/wp-content/uploads/2018/05/btbike_detail1.jpg) 那么是什么让这些转向灯如此特别呢？首先，他想把它做好，这样就没人想偷他的装置了。他希望主信号可以很容易地移除，这样他就可以把它带进去，控制装置也可以很好地集成到自行车上，这样就不会很明显。最后，他设法把一个电池组、Arduino Nano 和一个 HC-05 模块塞进了车把里；只有一个开关从最末端伸出来，暗示所有东西都没有库存。

另一边，一个 ATMEGA328P 微控制器和另一个 HC-05 驱动两个 8×8 LED 矩阵和 MAX7219 控制器。一切都由 18650 锂离子电池供电，134N3P 模块使其达到 5 VDC。为了使设备易于拆卸，并防止元件进入，所有硬件都封装在一个商用防水外壳中。作为最后一步，[西蒙]在混音中加入了 Qi 无线充电接收器，这样他就可以将信号取出，放在充电板上，而无需打开它。

我们已经有一段时间没有看到自行车转向灯了，所以很高兴看到用更现代的硬件制作的转向灯。但真正的问题是:[为了增加安全性，他会戴上发光头盔吗？](https://hackaday.com/2018/02/28/cheap-and-easy-helmet-lights-for-the-kids/)

 [https://www.youtube.com/embed/XL1OTpryOkE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XL1OTpryOkE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

