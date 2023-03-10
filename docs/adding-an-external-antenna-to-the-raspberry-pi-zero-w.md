# 为 Raspberry Pi Zero W 添加外部天线

> 原文：<https://hackaday.com/2017/03/07/adding-an-external-antenna-to-the-raspberry-pi-zero-w/>

在单板计算机上安装完整的 WiFi 子系统绝非易事，而在 Zero W 这样紧凑的主板上，这是一项了不起的成就。天线是个棘手的部分，因为铜走线只能做这么多。

新的 Raspberry Pi Zero W 的天线非常创新，但有时你需要一个外部天线来伸出手触摸某人。幸运的是，[给 Zero W](http://www.briandorey.com/post/Raspberry-Pi-Zero-W-external-antenna-mod) 增加一个外部天线一点也不困难，正如【Brian Dorey】向我们展示的那样。Pi Zero W 的设计师考虑周到地为超微型表面贴装超高频插孔提供了焊盘。插孔焊盘非常靠近长而弯曲的走线，作为板载天线的馈线。甚至还有一个零欧姆 SMT 电阻，可以稍微重新定位，以向 UHF 插孔馈送 RF。用烙铁和[Brian]的 Pi 连接到外部天线做了一点工作。

[Brian]包括测试数据，但除了一些异常值，外部天线似乎没有提供巨大的优势，至少在他的测试条件下。这说明了天线的创新设计，来自 Raspberry Pi 基金会的罗杰·桑顿(Roger Thornton)在上周的黑客聊天中讨论了这一设计。查看[档案](https://hackaday.io/event/20043/logs)了解更多信息。

感谢[工程师]的提示。