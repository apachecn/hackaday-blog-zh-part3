# OBD2 项目的实时 ECU 模拟器

> 原文：<https://hackaday.com/2017/07/10/a-live-ecu-simulator-for-obd2-projects/>

如果您正在使用 OBD2 硬件或软件，访问测试数据非常容易，只需将 OBD2 插座插入汽车即可。然而，如果您希望在发动机可能经历的所有可能的故障条件下测试 OBD2 软件，您将面临一个问题，即在不损坏发动机的情况下模拟运行中发动机的所有故障变得很困难。这导致[Fixkick]使用二手福特 ECU 创建了一个 OBD2 模拟器[,该 ECU 提供了来自 Arduino 的虚假传感器数据](http://www.fixkick.com/ELM327/taurus-sim/hacked.html),以说服它连接了一个真实的引擎。

这篇文章是一大堆很难读懂的文字，但是如果你是 ECU 黑客世界的新手，它提供了一些有趣的信息。其中描述了如何模拟曲轴和凸轮轴传感器，以及质量空气流量传感器、节气门位置和速度计传感器。一些 ECU 输入需要过零信号，这可以通过使用小型隔离变压器来实现。其结果是一个包含 ECU 和 Arduino 的盒装单元，其前面板上有电位计来改变各自的传感器输入。

这些年来，我们已经为您带来了相当多的 OBD2 项目，例如，有[这个 LED 转速表](http://www.fixkick.com/ELM327/taurus-sim/hacked.html)，以及[进入通用汽车的 OnStar](http://hackaday.com/2010/03/16/follow-up-hacking-onstar/) 。

谢谢你的提示。