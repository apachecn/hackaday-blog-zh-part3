# 一个 ESP8266 能低到什么程度？

> 原文：<https://hackaday.com/2018/01/22/how-low-can-an-esp8266-go/>

鉴于硬币电池的挑战，我们最近已经开始关注硬币电池的设计，因此我们对[CNLohr]的最新视频感兴趣，该视频是关于[用硬币电池将 ESP8266 推入尽可能低的电池消耗中](https://www.youtube.com/watch?v=I3lJWcRSlUA)。结果是一系列黑客攻击，基于逆向工程库并依赖于修改后的路由器，但这使功耗降低了十倍以上！

虽然 ESP8266 有一个深度睡眠模式，仅消耗 20 微安左右，但这并不像它看起来那么美好。如果你能睡一会儿，醒来一会儿，发送你的数据，然后继续睡觉，这可能是一件事。但是当你使用传统技术时，设备被唤醒，并且必须做大约十秒钟的工作(在高功率下)来连接到附近的接入点。然后它可以做你想做的事情，继续睡觉。那十秒钟的打击对小电池来说是致命的。

因为这就是你对标准库所能做的一切，下一步就是找到[pvvx]，他对大量的库进行了逆向工程，并提供了一个没有 [WiFi 功能](https://github.com/pvvx/SDKnoWiFi)的库。这是一把双刃剑。好处是你从深度睡眠中得到 30 毫秒的启动时间。不好的一面是，你没有无线网络。

因为如果你需要网络，这不是一件好事，[pvvx]也有一个最小版本的 SDK，它可以在大约 100 毫秒内唤醒并处理一个事务。更重要的是，在整个 100 毫秒内，功率消耗并不是 100%。该库使用不同的 TCP/IP 堆栈( [lwip](http://lwip.wikia.com/wiki/LwIP_Wiki) )来实现这一点。

这又要求无线路由器上有一个特殊的固件，因为没有足够的时间来完成整个 WiFi 事务。幸运的是，带有 OpenWRT 的路由器很容易被破解并按要求工作。[CNLohr]将数据从路由器发送到一个[谷歌表单](https://docs.google.com/spreadsheets/d/1oay41nWtpytSJAVGPSehMkfOp5g8D0GKNWIzqUzic_0/edit#gid=1212757165)。不寻常但有效。

[CNLohr]对 Hackaday 的页面并不陌生，他在 ESP8266 等方面做了很多工作。例如，我们喜欢他的 [USB 黑客](https://hackaday.com/2016/08/09/cnlohr-esp8266-usb/)。他还为这个无处不在的设备添加了 T2 有线以太网 T3。

 [https://www.youtube.com/embed/I3lJWcRSlUA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/I3lJWcRSlUA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

