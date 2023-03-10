# 模拟内脏显示 GPS 速度在这个混合速度计

> 原文：<https://hackaday.com/2016/06/28/analog-guts-display-gps-velocity-in-this-hybrid-speedometer/>

数字仪表盘很酷，但模拟仪表有持久的吸引力。直接连接到车辆变速器的纯机械仪表非常简单。当然这不是这里发生的事情。取而代之的是，这个建筑[是 GPS 获取的速度数据](https://github.com/RexFuzzle/AnalogGPSChrono)的模拟显示器。

下面的视频很好地解释了[格兰特·斯蒂芬斯]的基础。显示器本身是一个内置的船用速度计，装有来自摩托车转速表的运动。转速表设计用于接收 4 伏峰峰值方波输入信号，其频率与发动机转速成比例。为了显示道路速度，[Grant]将一台带有 GPS 模块的 ATTiny85 塞进仪表，并编写了一个脚本，将 GPS 速度数据转换成方波。显然有一些延迟，量表似乎不能很好地记录低速，但总而言之，一旦你转换成公制，它似乎很好地匹配股票 speedo。

还有很大的改进空间，但我们可以看到 GPS 数据的模拟表示在其他应用中也很有用。模拟仪表数字化非常有趣——就像这些旧仪表和仪表用来显示网上搜集的天气数据。

 [https://www.youtube.com/embed/pP-rwahyP9g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/pP-rwahyP9g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

