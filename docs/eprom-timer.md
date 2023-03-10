# EPROM 定时器

> 原文：<https://hackaday.com/2016/04/07/eprom-timer/>

[glitch]有一个便宜的 EPROM 橡皮擦，功能很少。事实上，这可能给了它太多的信任:它只不过是一个当它插上电源时打开，当它拔掉电源时关闭的紫外线灯。当然，实现一些安全功能会很好，所以他决定将它连接到一个[软件控制的电源插座](http://www.glitchwrks.com/2016/03/21/eprom-timer)。

当然，控制连接到电源的继电器在这里是老生常谈，事实上，我们已经讨论过[【glitch】的光隔离电源开关](http://hackaday.com/2013/03/05/24v-relay-driver-circuit/)。不过，这次他已经超越了正常的电源继电器项目。[glitch]没有使用微控制器来运行继电器，而是在他的计算机上编写了一个简单的 Ruby 脚本，在擦除内存所需的精确时间内打开 EPROM 擦除器。Ruby 脚本通过 USB 转串行适配器的 RTS 握手引脚直接驱动继电器控制。

[glitch]的黑客提醒我们，如果你只需要一点点慢速输出，USB 串行转换器可能就是合适的选择。你可以想象驱动从标准[灯](https://hackaday.com/2014/09/07/infrared-controlled-light-switch/)到你的 [3D 打印机的床加热器](http://hackaday.com/2015/12/16/mains-powered-3d-printer-heated-beds/)的所有东西(前提是你使用类似的硬件)，但这对声称完成任务后忘记关闭橡皮擦的【小故障】特别有帮助，这会留下一个潜在危险的紫外线源。给危险的设备增加安全功能总是一个好主意！