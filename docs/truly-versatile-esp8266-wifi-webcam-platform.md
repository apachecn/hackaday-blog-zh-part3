# 真正多功能的 ESP8266 WiFi 网络摄像头平台

> 原文：<https://hackaday.com/2016/01/24/truly-versatile-esp8266-wifi-webcam-platform/>

[Johan Kanflo] [建造了一个可爱的基于 ESP8266 的小无线摄像机](http://johan.kanflo.com/building-a-low-cost-wifi-camera/)。这是一个漂亮的小设置，而且它是完全开放的，附带[工作演示代码](https://github.com/kanflo/esparducam)是蛋糕上的肉汁！或者土豆上的糖衣。或者什么的。

[Johan]的设置将一个 ESP8266-12 模块与一个 [Arducam](http://www.arducam.com/) 配对，它看起来基本上像一个用于无处不在的小型 CMOS 图像传感器的 SPI 分线板。该板自然有一个电源和头编程的 ESP 模块以及大量的连接器。插入一些摄像头代码，你就有了一个定制的无线网络摄像头。相当狡猾。

[![pogo_pin_anim](img/605ef4ed0943a91b07fe973d213c4f42.png)](https://hackaday.com/wp-content/uploads/2016/01/pogo_pin_anim.gif) 但是由于【Johan】设计了 ESP-8266 板，其标准母接头连接到 ESP，因此它也可以[用作通用 ESP 开发板。](http://johan.kanflo.com/a-versatile-esp8266-development-board/)【约翰】制造了一些子板来配合它，包括一个钉床 ESP8266 测试仪(因为你永远不知道你什么时候会得到一个无用的 ESP 单元)和 WiFi-to-RFM69 无线电桥。对于一个整洁的小系统来说，这是两个非常棒的应用程序，并且提醒您在设计自己的项目时要考虑可扩展性。

我们之前报道过[Johan]的[sky grazer](http://hackaday.com/2015/12/31/art-for-planespotters/)项目，该项目在飞机飞过头顶时对其进行跟踪，并在一台破旧的 Mac 电脑上显示出来。那么，他也[创造了一个 ADS-B 控制的 moodlight](http://johan.kanflo.com/commercial-pilots-control-my-moodlight/) ，这有什么好惊讶的吗？这家伙着火了！