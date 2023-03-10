# Pi 零容量存储相框

> 原文：<https://hackaday.com/2016/03/25/the-pi-zero-mass-storage-picture-frame/>

Raspberry Pi Zero 和不会永远缺货的 Raspberry Pi A+只有一个 USB 端口，但这个端口背后有很多功能。这是一个 OTG USB 端口，就像你的智能手机上的 USB 端口一样，这个小插头可以成为任何类型的 USB 设备。将 Pi 转换为 USB 小工具可以让它成为串行连接、MIDI 设备、音频源或接收器，或者 USB 大容量存储设备。

[Francesco]对 Raspberry Pi Zero 的 USB 大容量存储功能特别感兴趣，并构建了一个小项目来展示其功能。他把一个π0 变成了一个数码相框的控制器，[不断地在一个小屏幕上显示所有的图像文件](http://garagetech.tips/pizero-on-digital-frame/)。

构建从[ [Andrew Mulholland]的 Pi 零 OTG 模式指南](https://gist.github.com/gbaman/4c1345c0c4d6d82149d4)开始，只做了一些修改。当 Pi 插入 PC 时，它会自动变成 100 兆字节的 USB 存储设备。无论如何，你不需要在数码相框上有那么多空间。

虽然设置一个数码相框很容易，但将 Pi Zero 用作 USB 小工具仍有大量未开发的潜力。通过足够多的按钮、开关和传感器，Pi 可以成为一个可穿戴的 MIDI 设备，或者通过 Pi 摄像头模块，成为一个 IP 网络摄像头。很棒的东西，我们迫不及待地想看看社区下一步会想出什么。