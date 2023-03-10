# ESP32 的开发框架达到 2.0

> 原文：<https://hackaday.com/2017/04/23/esp32s-dev-framework-reaches-2-0/>

去年我们一直在关注 ESP32 芯片的发展，但老实说，我们对扔掉所有友好的 ESP8266s 有点谨慎。本月早些时候， [Espressif 发布了他们的物联网开发框架](http://espressif.com/en/media_overview/news/esp-idf-20-released) (ESP-IDF)的 2.0 版本，如果你没有跟随，你会错过很多。

我们上一次认真审视 IDF 是在[芯片还是全新的时候，当时框架还在起步阶段](http://hackaday.com/2016/09/15/esp32-hands-on-awesome-promise/)。当时还没有对 I2C 等细节的支持，但你可以让两个内核都启动并运行，然后把它连接到网络上。我们想测试节能模式，但也没有实现。简而言之，我们从第一天开始就在看一座固件摩天大楼的建设，只有地基已经浇筑完毕。

但是八个月的变化有多大啊！查看发布版的 [GitHub 变更日志，这是一个全新的游戏。不仅有用于 I2C、I2S、SPI、DAC 和 ADC 等的驱动程序，还有上述产品的工作示例和文档。自然，也有大量的错误修正，特别是在复杂的 WiFi 和蓝牙低能耗栈中。当然，仍有工作要做，但 Espressif 似乎认为这个框架已经足够成熟，他们已经在芯片上开放了](https://github.com/espressif/esp-idf/releases/)[他们的安全漏洞奖励计划](http://espressif.com/en/media_overview/news/esp32-security-bug-bounty-program-launched)。是时候进行黑客攻击了！

如果你想要快速入门指南，你要找的文件在 GitHub 的[文档文件夹](https://github.com/espressif/esp-idf/tree/master/docs)里。如果你试图管理 ESP-IDF 的先前安装，你会注意到 V2.0 需要一个更新版本的 GCC 编译器，所以如果你想让它与 V1.0 安装共存，需要做一点[的工作。但我们认为你能处理好。](http://www.lucadentella.it/en/2017/04/15/esp32-14-esp-idf-v2-e-come-gestire-le-diverse-versioni/)