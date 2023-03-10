# OpenThread，物联网的解决方案

> 原文：<https://hackaday.com/2016/05/30/openthread-a-solution-to-the-wifi-of-things/>

“物联网”一词诞生于 1999 年，远在每台笔记本电脑都有 WiFi、每家星巴克都为喝拿铁咖啡的大众提供互联网之前。随着时间的推移，物联网意味着所有这些设备都将通过 WiFi 连接。为什么，没人知道。WiFi 对于物联网来说很糟糕——它需要太多的电力，覆盖范围不是很大，而且已经有太多的机器和路由器在 WiFi 网络上了。

这些年来，对于物联网的这个问题，有许多解决方案，但没有一个流行起来。现在，终于，可能有一个解决方案。Nest 与 ARM、Atmel、dialog、高通和 TI [合作发布了 OpenThread](https://github.com/openthread/openthread) ，这是一个线程网络协议的开源实现。

OpenThread 的物理层是 802.15.4，ZigBee 基于同一层。与 ZigBee 不同，OpenThread 的第四、第五和第六层看起来更像互联网的其他部分。OpenThread 具有 IPv6 和 6LoWPAN，真正的网状网络，并且只需要对现有的 802.15.4 无线电进行软件更新。

OpenThread 与操作系统和平台无关，通过抽象层连接不同的无线电应该相对容易。无线电和网络一直是物联网的问题，有了 OpenThread——尤其是支持它的公司——这些问题可能不会太久。