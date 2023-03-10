# 降低智能开关的功耗

> 原文：<https://hackaday.com/2016/07/07/dumbing-down-a-smart-switch/>

如今，万物互联是家庭自动化的发展方向。ITEAD 制造了一个 ESP-8266 开关，可以将你的电器物联网。如果你仍然有一个古老的 433 MHz 风格的无线电开关系统，他们甚至制作了一个 WiFi *和* 433 MHz 的系统。但是如果你太便宜而不能支付双模式版本，你总是可以自己添加一个 1 433 MHz 的收音机。或者至少，[就是这么做的【补锅匠】](http://tinkerman.cat/adding-rf-to-a-non-rf-itead-sonoff/)。

除了拆卸和逆向工程支持 WiFi 的交换机，[补锅匠]还将定制固件刷新到交换机的 ESP-8266 中，并将其全部集成到他现有的家庭[Node-RED](http://nodered.org/)框架中。现在，他有了更多打开客厅灯的方法，这是任何人都想不到的！

如果你想进入这个基于 WiFi 的家庭自动化游戏，你可以看看我们不久前在 MQTT 上运行的[系列。看到[Tinkerman]的 Node-RED 演示让我们想到，我们也必须给我们的家庭系统一个这样的外观。](http://hackaday.com/tag/minimal-mqtt/)