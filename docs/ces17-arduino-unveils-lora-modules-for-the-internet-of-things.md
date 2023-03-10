# CES17: Arduino 推出物联网 LoRa 模块

> 原文：<https://hackaday.com/2017/01/06/ces17-arduino-unveils-lora-modules-for-the-internet-of-things/>

WiFi 和蓝牙从来就不是十亿个物联网使用的无线电设备帽子、雨伞、灌溉系统或任何其他使世界范围内的事物网络变得有趣的设备。物联网的最佳无线电是在亚千兆赫范围内运行的轻量级无线电，不需要大量带宽，也不像 WiFi 那样消耗功率。在过去几年中，一种新的低功耗无线通信标准已经出现，现在这种协议——LoRa——将很快以 Arduino 的形式出现。

### 普里摩和 NRF

 [![primocore2](img/c84a7e9251f0970d8e2f15f05af363af.png "primocore2")](https://i0.wp.com/hackaday.com/wp-content/uploads/2017/01/primocore2.jpg?ssl=1)  [![primocore1](img/1e6b26ac0ed620c4e1c784ac06d8b049.png "primocore1")](https://i0.wp.com/hackaday.com/wp-content/uploads/2017/01/primocore1.jpg?ssl=1)  [![arduino-primo](img/f56e392681abeb4a4b236b4da7decdcc.png "arduino-primo")](https://i0.wp.com/hackaday.com/wp-content/uploads/2017/01/arduino-primo.jpg?ssl=1) 

它不是 LoRa，但 Arduino Primo 系列基于 ESP8266 WiFi 芯片和一个用于蓝牙的 [Nordic nRF52832](https://www.nordicsemi.com/eng/Products/Bluetooth-low-energy/nRF52832) 。Primo 采用了人们熟悉的 Arduino 外形，但它并不意味着是一款“物联网”设备。相反，它是一个用于需要上网的设备的微控制器。

今年在 CES 上展出的还有 Primo Core T1，我们第一次看到它是在五月的 BAMF。这是一个仅比美国 25 美分硬币大一点的棋盘，但它的袖子里藏着一些小把戏。Primo 核心围绕 nRF52832 构建，在一平方英寸的玻璃纤维上增加了湿度、温度、3 轴磁力计和 3 轴加速计。

Primo 核心有一些机械技巧。那些围绕圆周的齿形引脚可以焊接到 [Alice Pad](http://www.arduino.org/products/boards/arduino-alicepad) 上，这是一个分线板，增加了 USB 端口和 LiPo 电池充电器。

### 劳拉

 [![nodeshield2](img/053b43264e8a124c9a9a614d841ffe02.png "nodeshield2")](https://i0.wp.com/hackaday.com/wp-content/uploads/2017/01/nodeshield2.jpg?ssl=1)  [![gateway-shield](img/57f1e813daf1da6b898cb81ae77b38d0.png "gateway-shield")](https://i0.wp.com/hackaday.com/wp-content/uploads/2017/01/gateway-shield.jpg?ssl=1)  [![nodeshield](img/e0d3e2026827a4a970402bc325d2a23b.png "nodeshield")](https://i0.wp.com/hackaday.com/wp-content/uploads/2017/01/nodeshield.jpg?ssl=1) 

Arduino 套房的甲板上还有两个 LoRa 护盾。在与 Semtech 的合作中，Arduino 将在今年晚些时候发布这对 LoRa 护盾。第一个是节点屏蔽，简单到不能再简单了——它只是一个带有 LoRa 无线电和几个连接器的屏蔽。第二个是网关屏蔽，正如它在 tin 上所说的那样:它被设计成从其他 Arduino 设备(例如，以太网或 WiFi)到节点屏蔽的网关。这些板没有完全组装，但从我看来，Gateway shield 支持 GPS 芯片组和天线的能力明显更强。

### 与 Cayenne 和 MyDevices 的合作

当然，物联网如果不能轻松管理，也是一文不值的。Arduino 已经与 MyDevices 建立了合作关系，将一堆低带宽的无线电和串行连接变成易于使用的东西。我们已经看到了一些使用 MyDevices 的构建和项目，但是我看到的演示非常容易理解，即使房间里有太多的设备。

如果你正在研究下一个伟大的物联网，所有这些都是好消息。Primo Core 是我见过的最小的无线微控制器设备之一，LoRa Arduino shields 的加入意味着我们可能会在不久的将来看到有用的低带宽网络。