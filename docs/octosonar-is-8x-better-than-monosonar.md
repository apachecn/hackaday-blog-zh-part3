# 八声纳比单声纳好 8 倍

> 原文：<https://hackaday.com/2017/02/25/octosonar-is-8x-better-than-monosonar/>

HC-SR04 声纳模块价格低廉，经过一些哄骗，可以很好地帮助你的机器人测量到最近的墙壁的距离。但是，当易贝的卖家把这些东西装成十个装的时候，你为什么不在你的“机器人”上只装一两个呢？ [Octosonar](https://hackaday.io/project/19950/instructions) 是一个硬件和 Arduino 软件库，可让您在短时间内安装并运行多达八个声纳传感器。

Octosonar 使用 I2C 多路复用器发送“开始”触发脉冲，并使用八路“或”门将“回声”信号返回给主机微控制器。[软件库](https://github.com/arielnh56/SonarI2C)然后发送 I2C 命令来选择和触发声纳模块，几个中断例程观察“回声”线来计算飞行时间，从而计算距离。

在矩形机器人的每一边安装两个声纳可以让它以一种简单的方式平行于墙壁移动:转向或远离墙壁，直到它们匹配。观看下面的视频演示这个非常简单的设置。(还要注意机器人的 45 度盲点在哪里:撞-撞-撞！)

利用 I2C 多路复用器上的三个地址位，您可以向一个项目添加另外八个 sonars，同时只需要从您的主机微控制器多一个中断引脚。见鬼，以这些东西的价格，为什么不买全 64 呢？！

 [https://www.youtube.com/embed/Gm4uhaZJVkc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Gm4uhaZJVkc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



这个项目的评论建议了几个可供选择的方法:一对不同的标准多路复用器而不是 I2C，一个 CPLD 来处理逻辑，或者其他什么。但是如果你只是想要一个简单的设置，Octosonar 可以满足你。如果你想深入研究 HC-SR04 模块，请查看这个[完整的逆向工程和大脑移植](http://hackaday.com/2014/03/17/good-vibrations-giving-the-hc-sr04-a-brain-transplant/)或这个[类似的模块剖析](https://hackaday.io/project/5903-sonar-for-the-visually-impaired/log/18329-ultrasonic-module-virtual-teardown)并提供很好的参考。