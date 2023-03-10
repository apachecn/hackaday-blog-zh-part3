# Rube-Goldberg Overdrive 中的万圣节门铃道具

> 原文：<https://hackaday.com/2015/11/14/halloween-doorbell-prop-in-rube-goldberg-overdrive/>

[Conor]将他的 3D 打印棺材门铃连接到一组 RGB LEDs，一个尖叫的扬声器和一个无绳螺丝刀上的旋转头骨，以制造一个“快速”的万圣节恐慌。在这个过程中，他包括了 Adafruit 模块目录的一半，一个继电器电路板，以及 ESP8266 WiFi 模块，一个香蕉 Pi，以及更多不同形状和大小的 Arduinos，你可以摇一摇棍子。

我们的头旋转，不像[康纳]的尖叫头骨，只是[阅读这个鲁布·戈德堡安排](http://conoroneill.net/all-the-tech-behind-our-halloween-hallway-of-horror/)。(我们确信这对构建者来说是一半的乐趣！)有就抽吧！

从 RGB LEDs 开始；[Conor]没有直接控制它们，而是将它们连接到一个支持 WiFi 的条形控制器上。太好了，现在他可以通过无线电波控制这个地带了。但是控制协议是封闭的，所以他花了一周时间学习 Wireshark 嗅探网络数据，然后写了一个 Bash 脚本发送相关的 UDP 包来开灯。但这还不够花哨，所以[康纳]用 Go 重写了剧本。

是的，没错——Banana Pi 上的 Go 例程通过 WiFi 向 WiFi-LED-driver 桥发送自定义 UDP 数据包。让灯光闪烁。等到你看到头骨。

[![spooky_eye_anim](img/304c614df047d431ced52b00eee987b7.png)](https://hackaday.com/wp-content/uploads/2015/11/spooky_eye_anim.gif) 塑料头骨的每个乒乓球眼中都有新像素，由一个 Arduino Nano 和粘在头骨头部的电池控制。头骨被粘在一个无线钻机的驱动钻头上。一个继电器板和另一个 Arduino 让它在门铃响起时触发 10 秒钟。最后(等着吧！)连接到门铃的 Arduino 发出信号，并将导线设置为高电平，所有其他 Arduini 和 Banana Pi 都连接到该导线。

温和的黑客读者，现在不是“我可以用 555 和一些口香糖做到这一点”的时候现在是尽情享受这一切的时候了。因为万圣节结束了，我们确信[Conor]已经拔掉了所有的电路板和 Arduini，并把它们用于他的下一个项目。现在他对嗅探 UDP 数据包略知一二。

 [https://www.youtube.com/embed/FClhSNwFfT0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FClhSNwFfT0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

