# 粒子引入新硬件，增加网格支持

> 原文：<https://hackaday.com/2018/02/13/particle-introduces-new-hardware-adds-mesh-support/>

人人喜爱的 WiFi 和蜂窝物联网模块制造商 Particle 公司[正在推出他们的第三代硬件](https://www.particle.io/mesh)。粒子氩、硼和氙是粒子在物联网开发板领域的最新产品，这次他们添加了一些令人惊讶的东西:网状网络。

[![New Particle boards named Argon, Boron, and Xenon](img/66ffaf25e1ae6e917f78b41d4b9aaa9d.png)](https://hackaday.com/wp-content/uploads/2018/02/3gndboard-condensed.jpg) 这三块新板都是围绕 [Nordic nRF52840](https://www.nordicsemi.com/eng/Products/nRF52840) SoC 构建的，包括一个 ARM Cortex-M4F，带有 1MB 闪存和 256k RAM。这款芯片支持蓝牙 5 和 NFC。Argon 通过 Espressif 的 ESP32 增加了 WiFi，Boron 通过 ublox SARA-U260 模块将 LTE 带到了桌面上，Xenon 放弃了 WiFi 和蜂窝网络，仅依赖蓝牙，但仍保留了网状网络。这种分割是有意义的；Particle 希望您购买大量氙模块来构建您的网络，并使用氩或硼模块连接到外部世界。

这些板的形状符合[阿达果羽毛标准](https://www.adafruit.com/feather)，这是一个足够好的标准，比带有偏移引脚的巨大 Arduino 护盾好得多。

特别令人感兴趣的是对网状网络的支持。对于物联网解决方案(无论是什么)，如果你有足够多的节点或覆盖足够大的区域，网状网络几乎是必不可少的。进入这种网状网络的技术被称为粒子网格，并建立在 [OpenThread](https://openthread.io/) 之上。虽然现在看到粒子的网状网络还为时过早，但我们真的很期待现实世界的实现。

这些主板的预订价格设定氩模块为 15 美元，硼模块为 29 美元，氙模块为 9 美元。7 月份发货。