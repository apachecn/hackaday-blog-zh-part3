# 电弧炉闭合回路

> 原文：<https://hackaday.com/2017/03/17/electric-arc-furnace-closes-the-loop/>

当我们想到电弧炉(EAF)时，脑海中浮现的图像是一台巨大的机器吞噬兆瓦的电力，同时将回收的金属转化为液体。[Gregory Hildstrom]做了一些工作，将其中一台机器缩小成实用的家庭版。[格雷格]是建立在由[[格兰特汤普森]，又名“随机之王”](http://hackaday.com/2015/06/16/mini-arc-furnace-melts-its-way-into-our-hearts/)和[大道](https://www.youtube.com/watch?v=L3t-jBATM0w)所做的工作之上。工业电炉是计算机控制的设备，小心地将可消耗的碳电极放入钢熔体中。这款机器为家庭游戏玩家带来了这些功能。

[Greg]从 TIG 焊接一个铝框架开始。电弧炉的 Z 轴上没有很大的力，所以他使用了类似于 3D 打印机中使用的步进器和丝杠排列。一个阿达果步进电机防护罩安装在 Arduino Uno 上来控制这只野兽。Arduino 读取电弧上的电压，并相应地调整电极高度。

这个电弧炉后面的电弧来自一台 240 伏的焊机。这就是[格雷格]遇到一些麻烦的地方。焊工通过他们的工作周期来评定等级。占空比是他们在十分钟内可以连续焊接的时间百分比。30%占空比的焊机在需要 7 分钟的冷却时间之前只能焊接 3 分钟。电弧炉需要 100%占空比的焊机，因为熔化几磅钢需要时间。[格雷格]经历了几个不同的焊机模型之前，他发现了一个可以处理的压力。

最终[格雷格]在他房子上的 240 伏主断路器过热并爆裂之前，熔化并煮沸了几磅钢。电弧炉对家用电器的要求可能有点高。

 [https://www.youtube.com/embed/nQpdjkX7qyU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/nQpdjkX7qyU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

