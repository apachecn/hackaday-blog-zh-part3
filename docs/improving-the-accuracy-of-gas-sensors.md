# 提高气体传感器的精度

> 原文：<https://hackaday.com/2017/07/13/improving-the-accuracy-of-gas-sensors/>

如果您需要一个传感器来检测某种气体，您可能会考虑 MQ 系列气体传感器。这些小金属圆筒包含一个加热器和一些电化学传感器。将加热器连接到电压，并将电阻的一端连接到 ADC，这样就有了一个针对酒精蒸汽、硫化氢、一氧化碳或臭氧的传感器，具体取决于您选择的传感器型号。

这些是简单的模拟器件，正如你所料，它们对温度和湿度都很敏感。[Davide Gironi]想要一个更精确的气体传感器，所以他开始有点过度工程化，将这些传感器的输出与温度和湿度相关联。

准确度和精确度是有区别的，如果你想校准气体传感器，你需要用来校准它们*。[Davide]没有找出已知精度的气体传感器，而是采取了简单的方法:他在这些传感器的数据表上绘制了曲线。它简单明了。*

这些数字被输入到 R 中，通过一点工作，[Davide]有了一个不同气体浓度对特定阻力的查找表。在测试这些传感器时，他发现湿度、温度和气体浓度之间的相关性更高，这是人们所期望的。

这些传感器的文件可以在[Davide]的网站上获得，他还提供了一个简洁的小视频，向每个人展示了这些计算过程。你可以看看下面。

 [https://www.youtube.com/embed/kageOcdcsbk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/kageOcdcsbk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

