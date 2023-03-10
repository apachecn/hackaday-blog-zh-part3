# 使用 ESP8266 与笔记本电脑电池对话

> 原文：<https://hackaday.com/2018/05/28/talking-to-laptop-batteries-with-the-esp8266/>

这不是你经常考虑的事情，但是现代消费者笔记本电脑电池是一项非常先进的技术。它不仅将几十瓦时的能量封装在一个相对较小和较轻的封装中，而且还具有集成诊断功能，以确保所有这些不稳定的锂电池都得到检查。由于规模经济(除非你试图从原始设备制造商那里获得它们)，它们广泛可用并且非常便宜，是为你的项目提供动力的非常有吸引力的选择。

当然，如果像(特里奥)一样，你身边有一堆东西，这也会有所帮助。出于我们不会进入的原因，他有一大堆宏碁 AL12x32 电池组，他想用它们来做一些事情，而不是收集灰尘。他的想法是将其中一个连接到太阳能电池板，并将其用作一些 ESP8266 项目的电源，但希望能够与电池交谈，以获得状态和诊断信息。在研究了电池使用的智能电池系统(SBS)协议后，他能够提出一些代码，让他使用他的 ESP8266 从电池组的机载电子设备中提取 37 个独立的信息字段。

[![](img/439cc965d87a9d65deefe6d0d34b25ce.png)](https://hackaday.com/wp-content/uploads/2018/05/espbat_detail2.png)

Battery consumption over time

用万用表摆弄了一下，才弄清楚在电池的 8 针接口上哪个针做了什么。其中两个引脚需要短接，以使双 12 VDC 引脚生效。从技术上讲，如果你想以一种低技术含量的方式利用电池，这就是你真正需要做的。但是，为了从电池中获取一些信息，[teliot]必须识别 SBS 数据所在的系统管理总线(SMBus)接口的两个引脚。

一旦他知道该用哪根针与电池通话，剩下的就相当容易了。SBS 是有据可查的，SMBus 接口与 I2C 非常相似。像现在所有酷孩子做的一样，他的代码将电池信息发布到 MQTT，在那里他可以绘制电池信息，并获得关于他的太阳能系统性能的精细信息。

这不是我们第一次看到黑客[通过 SMBus](https://hackaday.com/2017/12/30/laptop-with-raspberry-pi-inside-learns-to-speak-battery/) 争论笔记本电脑电池，但对一个话题有多种观点总是好的。如果你计划让这种事情成为你的标准锦囊妙计的一部分，你甚至可能想要花时间[建立一个专用的 SMBus 扫描器](https://hackaday.com/2016/09/03/tour-de-force-battery-hacking/)。

[通过 [/r/esp8266](https://www.reddit.com/r/esp8266/comments/8m7zhp/i_am_communicating_with_unopened_laptop_battery/)