# 两个伟大的收音机一起品尝伟大

> 原文：<https://hackaday.com/2016/07/15/two-great-radios-taste-great-together/>

[Johan Kanflo]发给我们他的最新配方:一部分 RFM69 亚千兆赫无线电收发器和一部分 ESP8266 模块的混合物。做出来的菜看起来绝对美味！

我们都被 ESP8266 带来的易用性迷住了——插上电源，就可以与现有的 WiFi 网络通话——但我们讨厌电池供电应用的功耗。WiFi 很耗电。尽管 ISM 频段无线电模块使点对点通信变得便宜且省电，但让它们与你的电脑通话需要一个适配器。

所以[Johan]将两种无线电结合起来，做了一个甜美的 ISM-无线电到 WiFi 桥。他的演示应用程序接收 ISM 频段上发送的任何数据，并将其推送给 WiFi 网络上的 MQTT 代理。硬件和[固件](https://github.com/kanflo/espism/tree/master/mqtt_sniffer)都在 GitHub 上。

我们一直想要一个这样的设备用于我们的家庭网络。恭喜，[Johan]让一切变得如此简单！