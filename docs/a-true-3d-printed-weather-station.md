# 真正的 3D 打印气象站

> 原文：<https://hackaday.com/2018/04/05/a-true-3d-printed-weather-station/>

如果“3D 打印气象站”这个词让你想到现成传感器的打印外壳，不要觉得不好。当我们第一次读到罗布·沃德发来的关于他最新项目的消息时，我们也有同样的想法。当然，他不会是说他*实际上*打印了一个重要气象站的所有主要部件，比如风向标、风速计或雨量计？

[![](img/77d5cc4d0987acd533967e63b98080e1.png)](https://hackaday.com/wp-content/uploads/2018/04/3dpweather_detail.jpg) 除外，仔细一看，[那正是*所做的*](https://www.thingiverse.com/thing:2849562)。气象站的每个部分都是在 OpenSCAD 中设计的，打印出来，并注入各种维生素，将它们变成功能性的硬件。有趣的是，大部分魔法都是通过简单的簧片开关和磁铁实现的。

例如，风向标使用八个簧片开关和一个嵌入式磁铁来将当前风向传达给处理用户界面的 Arduino Uno。风速，另一方面，它是用一个簧片开关完成的，因为它只需要计算转数来计算速度。

[Rob]确实通过使用现成的气压传感器“作弊”，但我们会给他一个通行证。除非有人想设计一个可打印的气压计，否则我们会认为这是可打印气象站的高水位标志。

这不是我们第一次看到 [DIY 风速计](https://hackaday.com/2016/02/07/another-use-for-old-hard-drive-parts-anemometer/)或[雨量计](https://hackaday.com/2017/07/31/low-cost-rain-gauge-looks-for-floods/)，不同复杂程度的。但是最终版本的简洁外观、OpenSCAD 源代码的完全开放性质以及较低的部件数量使其成为任何希望升级其家庭预测游戏的人的一个极具吸引力的选择。