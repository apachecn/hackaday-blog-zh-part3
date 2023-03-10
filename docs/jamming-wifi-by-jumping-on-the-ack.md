# 通过跳上 ACK 干扰 WiFi

> 原文：<https://hackaday.com/2017/02/03/jamming-wifi-by-jumping-on-the-ack/>

随着我们的电波中充斥着越来越多的无线连接设备，什么会破坏这个系统的问题变得越来越重要。这里有一个特别有趣的例子，因为概念证明表明，你不需要专门的硬件来实现它。[Bastian Bloessl]发现了对之前研究的一个有趣的调整，即[允许 Atheros WiFi 卡通过模糊 ACK 帧](https://www.bastibl.net/jamming-wifi/)来干扰 WiFi。

WiFi 协议规定了接收设备在执行纠错后发送的确认帧(ACK)。它基本上说:“是的，我得到了那个数据帧，它检查过了”。这种纠错过程被证明是[Bastian 的]技术的关键，因为它为攻击硬件提供了决定是否干扰 ack 的时间。

[Mathy Vanhoef]在 2014 年底提出的干扰技术[概述了持续干扰和选择性干扰](http://www.mathyvanhoef.com/2015/10/advanced-wifi-attacks-using-commodity.html)。选择性部分包括监听数据包并对其进行分析，以确定它们是否发往攻击者希望干扰的 MAC。问题是，当你的商用硬件已经解码了那个地址的时候，就已经太晚了。[Bastian]不是试图干扰数据帧，而是干扰接收器发回的 ACK。如果没有确认，发送方将不会传输任何新的数据帧，因为它认为接收端有问题。