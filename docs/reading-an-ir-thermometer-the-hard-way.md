# 艰难地读取红外温度计

> 原文：<https://hackaday.com/2016/05/12/reading-an-ir-thermometer-the-hard-way/>

MakeHackVoid maker space 的[Derryn Harvie]黑了一个 10 美元的红外温度计并让它与 USB 通信。听起来很容易？请继续阅读。

他打开它，希望找到并接入一条串行总线。但是他找不到，主控制器是一个 COB 斑点——藏在没有标记的黑色环氧树脂下面。通常这是一个死胡同。(我们已经看到了一些有趣的方法来用激光[去除环氧树脂滴](http://hackaday.com/2015/08/24/using-a-laser-cutter-to-decap-ics/)，甚至[集成电路](http://hackaday.com/2015/08/29/co2-laser-decapping-to-fix-soldering-mistake/)。)

但是[Derryn]走了自己的路——截取从微控制器到 LCD 显示器的数据，并使用另一个微控制器对其进行逆向工程。他刮掉了通向 LCD 显示器的轨道上的阻焊膜，并使用示波器来识别公共驱动线。然后，他使用一个函数发生器来激励每条 LCD 公共线和段线，以构建一个完整的矩阵，确定驱动这些段的所有组合。随着所有信息的解码，电线被焊接起来，这样他就可以连接一个 Arduino，被切断的轨道也被修复。

因为 LCD 是多路复用显示器，所以偏置电压有四个级别。幸运的是，他可以通过读取八条段驱动线，用尽 Arduino 上的所有模拟输入，提取大部分 LCD 信息。也许一个具有更多 ADC 输入的不同微控制器会允许他显示更多 LCD 功能。他以后可以升级他的升级。如果你有一个类似的黑客要实现，那么[【Derryn】的代码](https://github.com/harvie256/IR_Thermometer_LCD_Read)可能对开始有用。

感谢[csirac2]从 MakeHackVoid 向我们发送此技巧。