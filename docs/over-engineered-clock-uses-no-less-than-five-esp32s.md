# 过度设计的时钟使用不少于五个 ESP32s

> 原文：<https://hackaday.com/2017/11/27/over-engineered-clock-uses-no-less-than-five-esp32s/>

当[ Proto G ]参加一项指导竞赛，该竞赛的唯一要求是该项目必须是无线的；他做的[很有风格](https://www.youtube.com/watch?v=7cszRjhAN34&feature=youtu.be)。让我们先放一分钟，他为时钟的每个字符都使用了单独的 ESP32 板，一个用于小时，一个用于冒号，一个用于分钟，另一个冒号，然后是秒。如果你一直在数，那就是五个 ESP32s。但是，就像我们说的那样…把它放在一边，考虑到他使用三种不同的无线通信协议来使五个 ESP32s 相互适应:

1.  他的手机和一个信号塔相连。
2.  其中一个 ESP 连接到他的手机来获取时间。
3.  另外两个 esp 连接到他的手机，并通过电路板的内部通信协议 ESPNOW 向另外两个 esp 发送分钟和秒钟信息

如果你想知道的话。他使用的每块板都有有机发光二极管、电池、USB 转串行转换器，当然还有 ESP32。[ Proto G ]觉得他可以用椅子压碎其中一块板上的编程连接器，从而给他的项目增加一些复杂性。他不得不拿出烙铁和一些跳线来进行快速而有效的修理。

请务必查看他的[指导页面](http://www.instructables.com/member/Proto%20G/)，了解更多伟大的项目！