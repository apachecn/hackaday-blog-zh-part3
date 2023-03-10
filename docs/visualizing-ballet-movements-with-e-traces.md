# 用电子轨迹可视化芭蕾动作

> 原文：<https://hackaday.com/2015/11/15/visualizing-ballet-movements-with-e-traces/>

当我们想到可穿戴技术时，芭蕾舞鞋不是第一个想到的设备。事实上，【Lesia Trubat】的 [E-Traces](http://cargocollective.com/lesiatrubat/E-TRACES-memories-of-dance) pointé鞋可能是有史以来第一双“互联芭蕾鞋”这个项目捕捉舞者脚的运动和压力，并通过蓝牙将这些数据提供给手机。

这双鞋是基于 Lilypad Arduino 的克隆鞋，是为缝制可穿戴设备而设计的。似乎 3 个[力敏电阻](https://en.wikipedia.org/wiki/Force-sensing_resistor)被用作模拟压力传感器，测量舞者双脚施加在地面上的力。一个 [Lilypad 加速度计](http://lilypadarduino.org/?p=384)测量脚的加速度。

这些数据被整合到一个运行在 iPhone 上的应用程序中，该应用程序允许舞者根据他们的舞蹈动作“绘制”模式。这创建了基于所表演的舞蹈的运动视频，并且还收集了可用于事后分析舞蹈动作的数据。

虽然这些鞋子专注于芭蕾舞，但[Lesia]指出，同样的技术可以扩展到其他形式的舞蹈，用于训练和可视化目的。