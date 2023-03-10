# 这种 3D 打印的机器人吸尘器太烂了

> 原文：<https://hackaday.com/2018/02/24/this-3d-printed-robotic-vacuum-sucks/>

在你花了一点时间思考标题中使用的措辞后，看看这个由[king 3737]创造的[临时搭建的机器人真空。真空的整个主体是 3D 打印的，所有内部电子设备都是现成的模块化组件。我们不能说它与 iRobot 等类似的商业产品相比有多好，但自己构建一个并不难。](http://dp5.boards.net/thread/115/own-robot-vacuum-cleaner)

[![](img/d28c7c43b1cc935eba748f5fadccd675.png)](https://hackaday.com/wp-content/uploads/2018/02/3dvac_detail1.jpg) 这个看起来相当关注的机器人的身体是在 DMS DP5 打印机上打印的，这是一个巧妙的技巧，因为它只有 200 毫米 x 200 毫米的构建平台。一旦所有的零件都打印出来，3D 笔就被用来将各部分“焊接”在一起。最终结果看起来有点粗糙，但应该会产生与打印部件本身一样强的结合。

该机器人有四套超声波测距仪来探测墙壁和障碍物，尽管可能不在你预期的位置。机器人的右侧有两组传感器，而左侧只有一组。我们不确定不对称布局背后的原因，但推测机器更喜欢右转。

控制由 Arduino Mega 和永远可靠的 HC-05 蓝牙模块提供。编写了一个配套的 Android 应用程序，它允许配置机器人，而不必每次想调整设置时都插入 Arduino。

我们不能说我们已经在 Hackaday 看到了那么多 DIY 机器人吸尘器，但我们肯定已经为商业可用的型号展示了我们公平分享的 [hacks。](https://hackaday.com/2015/12/05/hacklet-87-roomba-projects/)