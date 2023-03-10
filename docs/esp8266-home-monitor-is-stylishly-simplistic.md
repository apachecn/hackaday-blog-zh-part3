# ESP8266 家用显示器时尚简约

> 原文：<https://hackaday.com/2017/11/20/esp8266-home-monitor-is-stylishly-simplistic/>

人们常说“少即是多”，我们认为 Thingiverse 用户[bkpsu]发布的别致的 ESP8266 环境监视器绝对符合这一要求。该设备被命名为“Kube”，是一个 3D 打印的白色立方体，中心有一个有机发光二极管显示器,[bkpsu]说这是专门为他妻子的批准而设计的。奇怪的是，她不喜欢墙上裸露的印刷电路板。

[![](img/8fa17c0b2cf1c38f3be3b0d63b653575.png)](https://hackaday.com/wp-content/uploads/2017/11/kube_detail.jpg)

Multiple Kubes allow for whole-house monitoring.

在里面，事情有点复杂。Kube 使用 NodeMCU 开发板和[bkpsu]设计的定制分线点与显示器和传感器接口。对于温度和湿度监控，Kube 使用的是一直很受欢迎的 DHT22，并且[bkpsu]提到他对运动传感器和直接控制 RGB LED 灯条等东西有未来的计划。Kube 收集的所有数据都通过 MQTT 传输到 openHAB。

在非常详细的 Thingiverse 页面上，[bkpsu]给出了他对该项目的设计目标的背景信息，打印出高质量外壳的提示，带有亚马逊链接的零件列表，以及完成所有布线的引脚信息。对于那些想要一个属于自己的 Kube 的人来说，PCB 甚至可以在 OSH Park 买到。

即使今天市场上有这么多家用监控和自动化产品，许多黑客还是不愿意购买交钥匙商业产品。但是我们认为结果是[黑客已经推出了他们自己的](https://hackaday.com/2014/12/06/raspberry-piphone-thermostat-monitors-your-entire-house-or-at-least-thats-the-plan/)解决方案，[他们可能会有所发现。](https://hackaday.com/2016/04/15/home-automation-and-monitoring-with-edison/)