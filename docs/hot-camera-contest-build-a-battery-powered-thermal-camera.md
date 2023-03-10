# 热感相机大赛:打造电池供电热感相机

> 原文：<https://hackaday.com/2018/07/18/hot-camera-contest-build-a-battery-powered-thermal-camera/>

这是对所有硬件黑客的挑战。彼得·詹森在 Hackaday.io 网站上举办了热感相机大赛,在一个电池供电的项目中使用热感相机。

这里的挑战很简单。在电池供电配置中使用 Flir 轻子热成像相机模块。不过，有一个问题:这是一个在*辐射*模式下使用轻子的项目，在这个项目中，相机为每个像素提供一个实际的温度值。是的，这是 Flir 轻子模块中有记录的功能，但迄今为止很少有人使用它，也没有人用小型电池供电的设备做到这一点。

这项挑战的规则是在辐射模式下使用 Flir 轻子 2.5，使用 Raspberry Pi Zero W 或 ESP32。这项挑战中的任何软件都必须以文本格式吐出绝对温度值，并且必须有将 Flir 轻子置于低功耗模式的演示。这里有两个挑战，一个是 Raspi，一个是 ESP32 获胜者将会被提名。

## 从迷人的传感器中获得更多

Flir Lepton 是一款非常小的热感相机，已经在创客社区上市一段时间了，最初是通过 [GroupGets](https://groupgets.com/) ，现在是通过 [Sparkfun](https://www.sparkfun.com/products/14654) 。对于一对本雅明来说，其规格非常令人印象深刻:轻子的分辨率为 60×80 像素，一切都可以通过 SPI 端口读取。轻子给任何项目热成像， [PureThermal board](https://www.sparkfun.com/products/14654) 把轻子变成 USB 设备。

Peter Jansen 是 2014 年 Hackaday 奖第四名[开源科学三录仪](https://hackaday.io/project/1395-open-source-science-tricorder)(没错，是三录仪)的创造者。你可以理解他是如何对便携感兴趣的，我们确信无论他对这个电池供电的前视红外有什么想法，都会很棒。

这确实是 Hackaday.io 社区能力的一个很好的例子。这里的目标是为一些非常有趣的硬件创建有用的开源驱动程序，并且有一些奖励来增加奖金。Peter 为两位获奖者每人提供了一张价值 125 美元的 Sparkfun 礼品卡。解决一个棘手的问题并使设计对其他人来说更容易的挑战是一个强大的动力。谁不喜欢挑战呢？