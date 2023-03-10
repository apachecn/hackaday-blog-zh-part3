# 一美元板针对学生

> 原文：<https://hackaday.com/2016/05/16/one-dollar-board-targets-students/>

树莓派被制作得很便宜，目的是让它们进入学校。但是针对嵌入式编程教学的项目呢？世界上有很多财政拮据的学校，教师自掏腰包购买教学用品的情况并不少见。你能用一块仅值一美元的板子做什么？

这就是团队推广“[一美元板](https://www.indiegogo.com/projects/one-dollar-board--3#/)”(我们不知道他们为什么不叫它巴克板)背后的想法。这个想法是为一个简单的微控制器板生产一个创作共用设计，只需要一美元。你可以在下面看到一个关于这个项目的视频。

尽管获得了知识共享许可，但我们找不到太多可用的细节。该板似乎使用 8 针 Atmel CPU(常见问题解答表明该板将使用 Arduino IDE)。我们猜测它本质上是一个安装了 V-USB 的 ATtiny85 的 [Digispark](http://hackaday.com/2012/08/13/teensy-tiny-arduino-board-with-an-attiny85/) / [Adafruit 小饰品](https://www.adafruit.com/products/1501) / [。](https://www.obdev.at/products/vusb/easylogger.html)

众筹活动页面列出了以下详细信息:

*   CPU: 8 位
*   GPIO(输入和输出端口):6
*   USB 接口:是
*   内存:闪存 8kb(可扩展至 256)
*   扩展空间:WiFi ESP8266，内存 24C256，H 桥 L293
*   电压:5V
*   指示灯 LEDs
*   重置按钮:是
*   安装空间:4(与 Arduíno UNO 或类似产品兼容)
*   快速指南:英文版附有其他语言的印刷指南。

如果*是基于 ATTtiny85 的设计，其中两个“GPIO”引脚将被 USB 编程器吃掉，可能还有两个被指示灯吃掉。并且 8 kB 闪存中的一些被引导装载程序消耗掉。简而言之，它不可能一次做所有的事情。尽管如此，它可能只是让你的脚湿的东西。*

但真正的故事是价格。当然，美元价格标签不包括运输或税收，但即使价格降得这么低也令人印象深刻。时间会证明市场是否对美元板感兴趣。如果非要猜的话，真正的价值会在现成的课程材料中。

那里有很多教育委员会，T2 有很多教育委员会，但是很少(如果有的话)是一分钱一分货的。

 [https://www.youtube.com/embed/6RejEmHYpo0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6RejEmHYpo0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

