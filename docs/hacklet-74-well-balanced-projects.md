# hack let 74–平衡的项目

> 原文：<https://hackaday.com/2015/09/11/hacklet-74-well-balanced-projects/>

平衡:我们人类想当然。如果没有内耳提供的平衡感，我们将很难站立或走动。对我们来说容易的事情对机器来说可能非常困难。平衡事物的项目长期以来一直是工程师、制造商和黑客的挑战。这是理所当然的，因为制造一台保持物体平衡的机器通常需要一些新颖的电子和机械解决方案。本周的 Hacklet 都是关于保持一个物体——或者它们自己——平衡的项目。

[![wheel](img/2256b4a784c221bb39659bb2b2c1a8a1.png)](https://hackaday.io/project/4267) 我们先从【曼努埃尔·卡斯滕】和[摆轮](https://hackaday.io/project/4267)说起。受混沌通信大会上一个项目的启发，[Manuel]创造了一个看起来永恒的黑客。一个不锈钢球被平衡在一个木轮上。该系统使用太阳能电池检测球的位置。电池上更多的光意味着球正在从轮子上滑落。该系统通过旋转轮子来对抗下落的球来抵消这一点。在过去，这将是一个模拟系统。[Manuel]通过使用 ATmega644p 处理器使事情变得更加现代。视频显示轮子旋转得有点快，因为系统被调整为乒乓球而不是沉重的钢辊。

[![sideway](img/dc5802ee72beb82d7220ef1fe6f88242.png)](https://hackaday.io/project/6999) 下一个出场的是【杰森·多利】。Sideway 是一种能够自我平衡的双轮滑板。这个项目最好的一部分是，大部分机械部件来自电动滑板车，这意味着它们很容易获得。框架甚至更简单:一块坚固的胶合板支撑着骑手和所有的电子设备。两个踏板车电机由剑齿虎 2x32A 电机控制器驱动。视差推进器执行平衡动作，从 ITG3200 数字陀螺仪和 ADXL345 加速度计获取 IMU 数据。速度是通过前后倾斜来控制的，就像赛格威一样。方向盘由 Wiimote 双截棍控制。Sideway 由 3 节脂肪电池供电。[杰森]说他每次开这辆车都会引起很多关注。

[![balance-robot](img/a24fbb7f7d73127d80d58a6520a84445.png)](https://hackaday.io/project/5872) 【多米尼克·罗比拉德】开发了他的[爬楼梯自平衡机器人](https://hackaday.io/project/5872)，作为他在渥太华大学硕士学位的一部分。我们不知道他的顾问给他打了多少分，但我们给这个项目打了 A+。机器人是一个四轮驱动的越野怪物。两个重型驱动马达使它转向坦克风格。机器人最令人印象深刻的部分是两臂，这使得它可以滚动整个底盘，越过可以阻止更大机器人的障碍物。[多米尼克的]机器人不仅仅是静态平衡，它还可以抬起来，像赛格威一样骑在两个轮子上。如果它真的翻倒了，手臂会把它抬起来！

[![terrabalance](img/3b822d92ff9784c256ee1047bdaf484a.png)](https://hackaday.io/project/4297) 最后，我们有【保罗布里斯托】与[太拉朋](https://hackaday.io/project/4297)。[Paul]得到了 CERN 开发的飞行时间(ToF)传感器 [TeraRanger One](http://www.teraranger.com/product/teraranger-one-distance-sensor-for-drones-and-robotics/?tra=3) 的早期副本。他决定用它在一根木棒上平衡一个乒乓球来测试一下。在这种应用中，传感器的速度必须大大降低，每秒钟只能读取大约 1000 次数据，然后取平均值。Arduino 从传感器读取距离数据，并使用该数据驱动业余爱好伺服系统。这里没有 PID 循环，事实上，Terabalance 是一个很好的例子，说明一个纯比例系统将如何永远搜索。也就是说，把球保持在平衡杆上就足够了。

Hackaday.io 上有大量的平衡项目，如果你想看到更多，请查看新的[良好平衡项目列表](https://hackaday.io/list/7622-well-balanced-projects)！我错过你的项目了吗？不要害羞，[在 Hackaday.io 上给我留言就行了](https://hackaday.io/adam)。这就是本周的 Hacklet，一如既往，下周见。同样的黑客时间，同样的黑客频道，带给你最好的 [Hackaday.io](https://hackaday.io) ！