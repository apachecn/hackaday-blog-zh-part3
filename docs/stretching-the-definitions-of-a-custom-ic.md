# 扩展定制 IC 的定义

> 原文：<https://hackaday.com/2018/05/20/stretching-the-definitions-of-a-custom-ic/>

Maker Faire 是所有新奇事物的纽带。在本周末的湾区创客大会上， [zGlue 推出了一个新平台，扩展了定制 IC 的定义](http://www.zglue.com/)。这是定制硅吗？不，一点也不。zGlue 是一个平台，允许任何人将现成的 IC 封装到单个模块中，允许您用更短的 BOM 构建更小的 PCB。

[![](img/6b033e3f0b2dcc222d75c9a41efbca4c.png)](https://hackaday.com/wp-content/uploads/2018/05/zgluethmb.jpg)

The zGlue module found in the zOrigin

zGlue 背后的想法是将今天可用的所有有趣的芯片从加速度计到集成无线的微型微控制器放在一个很小很小的板上，然后封装。在 Maker Faire 上，zGlue 团队正忙于展示他们基于云的平台，该平台允许任何人将现成的芯片添加到 zGlue 堆栈中，并将其组装成定制模块。

当然，每个新的科技创业公司都需要一个演示，所以 zGlue 推出了 [zOrigin，这是一个小型健身追踪器，它的特点是将一套芯片塞进一个封装包](http://www.zglue.com/technology#zorigin)。zOrigin ZiP 封装中包含的芯片包括一个带 BLE 的 Dialog DA14585 微控制器、一个 ADI 心率监控器、一个晶体、一个 Flash、一个电源监控 IC 和一个加速度计。在这个单个芯片中还有三十个无源器件，加上电池、一些 led 和振动电机，这个芯片成为可穿戴健身追踪器的完整解决方案。

将一堆芯片塞进一个模块并不是什么新鲜事；市场上大多数可用的无线模块就是这样。NextThingCo 试验了一台带有 GR8 模块的芯片上的 Linux 计算机，还是一堆涂有环氧树脂的芯片。定制模块最明显的好处可能是[成为掌上明珠的 Octavo 片上系统](https://hackaday.com/2017/04/15/an-even-smaller-beaglebone/)。

虽然从现成芯片创建定制模块的能力对制造商来说并不新鲜，但任何人创建自己的定制 IC 的能力对普通硬件黑客来说仍然遥不可及。zGlue 是这个问题的解决方案，价格似乎相当合理，初始研发费用从 100 美元左右开始。