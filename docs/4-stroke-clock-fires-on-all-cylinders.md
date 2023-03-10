# 四冲程时钟在所有气缸上点火

> 原文：<https://hackaday.com/2018/02/11/4-stroke-clock-fires-on-all-cylinders/>

我们喜欢这里建造的好钟，尤其是它以独特的方式报时。[这款由【lag Silva】](https://www.instructables.com/id/4-Stroke-Digital-Clock/)设计的 4 冲程数字钟在该类别中独树一帜。当它显示时间时，它也显示了内燃机的运行。这些数字以活塞的形式出现，没完没了地重复着进气、压缩、燃烧和排气。

时钟的数字由两个 LED 矩阵组成，由一个 Arduino Uno 和几个 MAX7219 驱动板驱动。构成数字的点按照 1-3-4-2 的顺序在矩阵中上下移动。当每个活塞数字到达上止点时，它的数字变亮。这使得很容易看到点火顺序，即使在较高的转速值。

我们最喜欢的是这个时钟的可变转速设置。后面有一个 10k 的罐子，可以在 100 到 800 RPM 之间调整活塞的速度，它的配置可以准确地表示活塞在每个增量上的运动。踩到底，看着时钟加速和减速。

虽然很难在 800 转/分钟时读取时间，但在客车的平均怠速下看到气缸运动的实时可视化效果非常棒。我们认为用另一种方式来加速引擎可能更好，比如用拱廊式油门杆或脚踏板。

如果你喜欢不断移动的时钟，但更喜欢模拟读数，[花一分钟看看这个没有面孔的时钟](https://hackaday.com/2018/01/09/edgytokei-time-on-the-edge/)。

 [https://www.youtube.com/embed/ZnF2L76vghc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZnF2L76vghc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

