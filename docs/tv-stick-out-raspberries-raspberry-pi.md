# 电视棒出来-树莓树莓 Pi

> 原文：<https://hackaday.com/2016/05/11/tv-stick-out-raspberries-raspberry-pi/>

基于 Android 的电视棒应该会出现在更多的项目中。它们容易获得且价格低廉。他们的价格马力很大，他们甚至可以启动一个主线 Linux 内核，不像我们知道的一些单板计算机。它们比圆周率零点小，所以几乎可以放在任何地方。

不过，他们唯一没有的是 I/O。当然，它有一个 USB 端口，但仅此而已。[死灵]考虑到这些问题，创造了一个载板来解决所有这些问题。

*   车载 3A DC-DC。你可以用 7 到 24 伏 DC 的任何电压为整个系统供电
*   一个 4 端口 USB 集线器
*   ATtiny 2313，通过 V-USB 堆栈连接到集线器
*   背面有 2 个 USB 端口，通过 GPIO 线进行电源控制
*   前面有一个 USB 端口(电源始终打开)
*   3 个继电器
*   适合普通阳极氧化铝外壳

[ATtiny 代码位于 GitHub](https://github.com/nekromant/tinypowerswitch) 上，允许完全 I/O 控制，将引脚状态保存在 EEPROM 中，并提供多达 8 个伺服控制通道。设备通过 USB 端口连接(占用集线器上的一个端口)。

将消费设备重新用于嵌入式服务并不是什么新鲜事。我们已经在手机上看到过这种情况。我们甚至看到了用作鼠标的[遥控器](http://hackaday.com/2012/07/19/use-your-tv-remote-as-an-hid-mouse/)。但是这是一个非常好的模板，可以为您的项目添加廉价而简单的计算能力，我们很惊讶我们没有经常看到它。你为什么不在你的项目中加入电视棒呢？