# Makerville Knit:工业级 WiFi 突破

> 原文：<https://hackaday.com/2016/04/05/makerville-knit-industrial-strength-wifi-breakout/>

如果你需要工业级的物联网产品，你需要工业级的 WiFi 芯片组。对于我们自己的家庭黑客来说，我们对 ESP8266 芯片非常满意。但是，如果你需要连接到巨大而可怕的互联网，你可能会想要最先进的加密技术。特别是，Amazon 坚持为他们的 Web 服务(AWS)使用 TLS 1.2，我们不知道如何在 ESP 上使用它。

[Anuj] [设计了一款名为 knit](https://makerville.io/knit/) 的分线板，其中包含一个 Marvell MW300 WiFi SOC。这款芯片有一个运行在 200 MHz 的板载 ARM Cortex M4F，这意味着你有很多东西可以玩:闪存，RAM，浮点单元，你能想到的。Marvell 有一个使用 AWS 的 [SDK，包括操作系统、外围设备支持和其他细节。包括 TLS 1.2。](https://github.com/marvell-iot/aws_starter_sdk/)

![Cd_tjKoWwAApnU9_thumbnail](img/3d90a555f3c8b40eca5a55b6f7cae2ce.png)最重要的是，MW300 breakout 价格合理(尽管自然比大规模生产的 ESP8266 模块贵)，而且[它是一个完全开放的设计](https://github.com/Makerville/knit)。[Anuj]似乎也在为生产做准备，如果你不想自己做的话。

MW300 出现在各种商业物联网设计中，它是一款久经考验的安全连接“云”的产品。唯一对业余爱好者友好的类似主板是[Adafruit wicked WiFi Feather](https://www.adafruit.com/products/3056?utm_source=youtube&utm_medium=videodescrip&utm_campaign=newproducts)，但它更贵，功能更弱，目前缺货，这正好表明了对这种东西的需求。

当然，如果你需要更多的集成外设，你可以[改装一个“你好芭比”玩具](http://hackaday.com/2015/11/24/hello-barbie-records-your-children/)，它也有同样的芯片、甜美的音频编解码器和一个漂亮的闪存 ROM。

我们认为,[Anuj]为这个强大的小 WiFi SOC 制造和测试突破是很棒的。我们的项目现在还不需要——我们正在完全不安全的模式下运行——但是知道你有什么选择是很好的。(我们也在研究 ESP8266 的[esp-open-RTOS](https://github.com/SuperHouse/esp-open-rtos)—我们知道他们一直在研究 TLS 1.2 加密，但我们不知道他们目前的状态如何。有人吗？)