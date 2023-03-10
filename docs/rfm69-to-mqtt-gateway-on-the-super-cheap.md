# RFM69 到 MQTT 网关上的超便宜

> 原文：<https://hackaday.com/2015/11/14/rfm69-to-mqtt-gateway-on-the-super-cheap/>

[Martin]正在开发 RFM69 到 MQTT 的桥接设备。如果你对 DIY 家庭自动化感兴趣，这将是值得遵循的。为什么？当你的家庭自动化网络变得足够大时，你将不得不认真考虑不同部分如何相互通信。有许多方法可以处理这个消息传递问题，但是 [MQTT](http://mqtt.org/) 无疑是一个竞争者。

MQTT 是一个“轻量级”的发布-订阅框架，旨在实现机器对机器的数据共享，并运行在普通的 TCP/IP 网络之上。IBM 从一开始就是 MQTT 背后的推动者，现在[亚马逊也在使用它](https://aws.amazon.com/blogs/aws/aws-iot-cloud-services-for-connected-devices/)。

但是大多数 MQTT 服务器需要一个 TCP/IP 网络，这很大程度上意味着 WiFi，这对于您希望使用电池供电或处理能力有限的远程传感器来说可能是一个杀手。对于这些用例，低功耗、简单的亚千兆赫无线电模块是比 WiFi 更好的选择。但是，如何让低功耗无线电与 MQTT 设备对话呢？

这就是[马丁]的 MQTT 桥的观点。此前，他为 Raspberry Pi 构建了一个 sub-gig 无线电附件，并让 Pi 处理网络。但是看起来低级的 ESP8266 有足够的处理能力来处理 MQTT 方面的事情(当然是通过 WiFi)。这意味着您现在可以将您的 868 MHz 无线电设备连接到 MQTT，花费比两杯南瓜香料双泵拿铁咖啡还少。

在固件方面，[马丁]得到了[费利克斯]的帮助，后者开发了 Arduino-plus-RFM69 项目，即 [Moteino](http://lowpowerlab.com/moteino/) 。[Felix]显然已经将他的 RFM69 库移植到了 ESP8266 上。我们迫不及待地想看到这个工作。

 [![esp8266_rfm69_veroboard](img/1ed17addc805bb060f0c0b583fb29116.png "esp8266_rfm69_veroboard")](https://hackaday.com/2015/11/14/rfm69-to-mqtt-gateway-on-the-super-cheap/esp8266_rfm69_veroboard/)  [![esp_mqtt-shot0001_tn](img/bc80f4b0ba08175a47db7f0df82e5122.png "esp_mqtt-shot0001_tn")](https://hackaday.com/2015/11/14/rfm69-to-mqtt-gateway-on-the-super-cheap/esp_mqtt-shot0001_tn/)  [![RFM69_mqtt](img/6220becc8195209e052c326d2ea4288a.png "RFM69_mqtt")](https://hackaday.com/2015/11/14/rfm69-to-mqtt-gateway-on-the-super-cheap/rfm69_mqtt/)  [![RFM69_serial_console](img/d4a8b44a9ad089c78d3c4f4262800a0d.png "RFM69_serial_console")](https://hackaday.com/2015/11/14/rfm69-to-mqtt-gateway-on-the-super-cheap/rfm69_serial_console/) 

现在，我们有一些提示性的截图，暗示了一些局域网暴露的配置屏幕。我们对 RFM + MQTT 调试控制台窗口特别感兴趣，它应该真正有助于找出跨两种无线电协议的系统中的错误。

所有这些的底线是什么？基于 RFM69 的超廉价、高能效无线电节点可以与您复杂的 MQTT 网络对话。关注这个项目。