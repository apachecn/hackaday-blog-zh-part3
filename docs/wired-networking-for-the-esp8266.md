# ESP8266 的有线网络

> 原文：<https://hackaday.com/2016/07/01/wired-networking-for-the-esp8266/>

越来越多的项目中出现了越来越流行的 ESP8266。有 CNC 控制器，blinkey WiFi 照明，和彻头彻尾的怪异 WiFi 到以太网桥。 [[Cicero]已经开始使用这些支持以太网的 ESP8266 构建，现在一切正常，组装简单，构建成本低廉。](https://github.com/Cicero-MF/esp_enc28j60)

敏锐的读者会注意到[我们在](http://hackaday.com/2016/04/01/ethernet-controller-discovered-in-the-esp8266/)之前见过类似的事情。几个月前，[cnlohr]在 ESP8266 中发现了以太网控制器。从各方面来看，这都是一种艰难的做事方式。[cnlohr]通过 ESP 的 I2S 总线直接驱动以太网。[西塞罗]的项目没有。它使用廉价的 ENC28J60 SPI 到以太网适配器将 ESP 放在有线网络上。一个解决方案比另一个好吗？那是有争议的。一个解决方案比另一个简单得多吗？是的，[Cicero]的工作允许任何人通过几个电阻和一个通常在线商店售价 3 美元的模块将以太网添加到 ESP8266 中。

有了来自[Ulrich Radig] 的以太网堆栈[，来自](http://www.ulrichradig.de/)[【MetalPhreak】](https://github.com/MetalPhreak/ESP8266_SPI_Driver)的 SPI 驱动程序，以及来自[Sprite_tm] 的基于 [ESP8266 的 web 服务器，【Cicero】设法通过有线和无线连接提供网页。](https://github.com/Spritetm/esphttpd)

虽然这种构建在技术上不如[cnlohr]直接从 ESP 驱动以太网的工作那样令人惊叹，但它非常容易实现，为有线 ESP 的一些更有趣的功能打开了大门。随着以太网的解锁，有一个免费的 WiFi 接口到 wardrive，在混杂模式下四处窥探，注入数据包，在网状模式下将一群 esp 桥接到另一个网络，以及其他网络恶作剧。ENC28J60 模块可能已经进入了一些零件箱和垃圾箱，使[西塞罗]的工作成为 ESP 有线网络的快速入门指南。

感谢[PuceBaboon]发送此邮件。