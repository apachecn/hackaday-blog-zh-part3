# 微芯片推出微型廉价 Linux 模块

> 原文：<https://hackaday.com/2018/02/24/microchip-introduces-tiny-cheap-linux-modules/>

如今，Linux 无处不在，这意味着设计师和工程师迫切需要一个简单易用的模块，来简化构建产品的设计，以便用 Linux 做一些事情。这种产品类别的最佳示例可能是 Raspberry Pi 计算模块，其次是 C.H.I.P. Pro 及其 GR8 模块。有几十种内部填充有 Allwinner 和 Mali 芯片的板可以用来构建 Linux 产品，如果你需要 Linux 并希望非常非常快地戳针，那么“片上 BeagleBone”是一种非常棒的产品。

现在微芯片推出了他们对 Linux 系统模块化的答案。[sama5d 2](http://www.microchip.com/design-centers/32-bit-mpus/sip-and-som/sip-som-overview)是一个 BGA 封装的单芯片，占地面积小，运行 Linux。它功能强大，价格低廉，如果您想在项目中使用 Linux，这是您的最新选择。

这个新的微芯片系列的核心产品是 [SAMA5D2 SIP](http://www.microchip.com/design-centers/32-bit-mpus/sip-and-som/system-in-package-(sip)) ，这是一个封装系统，将 ARM Cortex-A5 CPU 和 DDR2 存储器放在单个 BGA 封装中，粗略检查一下，看起来很容易设计 PCB 并进行回流。这一系列有四个芯片，128 兆位、512 兆位和 1 千兆位的 DDR2 内存。128 兆位的芯片是为裸机和 RTOS 应用设计的，更高的内存芯片至少能像一个重新设计的路由器一样运行 Linux。

该芯片是 Microchip 的 ATSAMA5D2 SOM 的核心，这是一个模块上的系统，它将电源管理(只需要一个 3.3V 电源)、以太网 PHY 和启动存储器添加到一个封装中，该封装可以像 QFN 封装一样有效地手工焊接。它是片上 Linux，或者至少是我们已经接近的概念。

将 Linux 添加到一个项目中是困难的，虽然有模块和系统可以做到这一点，但我们总是欢迎给设计师更多的选择。虽然这些模块和系统与强大的 ARM 微控制器相比并不便宜 SIP 的起价约为 9 美元，SOM 的 100 片订量价格为 39 美元——但与其他可用的 Linux-on-Modules 相比，这个价格相当低。