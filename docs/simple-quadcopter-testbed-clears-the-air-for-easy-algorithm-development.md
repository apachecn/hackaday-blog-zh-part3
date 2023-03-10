# 简单的四轴飞行器试验台为简单的算法开发扫清了障碍

> 原文：<https://hackaday.com/2018/06/28/simple-quadcopter-testbed-clears-the-air-for-easy-algorithm-development/>

我们不必告诉你，无人驾驶飞机风靡一时。但是，虽然新的商业模式一直在发布，制造商也发布了新的部件，但硬件中使用的基本技术在过去几年中没有改变。当然，我们增加了更多的传感器，增加了计算能力，提高了效率，但关键的发展来自软件:你只需要看看市场上最新的模型，或者 Git 提交 Betaflight，Butterflight，Cleanflight 等的频率。

考虑到这一点，[int-smart]正在为一个 Hackaday 奖项目开发一个用于开发算法的[四轴飞行器测试平台，特别是定位和地图。该项目的目标是最终尽可能容易地离开地面并开始编写代码，以及通过 ROS 将映射算法与 Ardupilot 集成。](https://hackaday.io/project/85715-quadrotor-testbed-for-localization-and-mapping)

最初的想法是使用 Beaglebone Blue 和一些便宜的业余硬件，这对于这种尺寸的无人机来说是相当标准的:1250 kv 电机和 SimonK ESCs，安装在 f450 火焰轮风格的框架上。然而，看起来一个现成的解决方案可能会更简单，如果它可以与 ROS 一起工作。Scanse Sweep 激光雷达传感器提供点云数据，然后通过一些迭代最近点(ICP)处理来咀嚼这些数据。如果你喜欢数学，那么绝对值得一读项目日志，因为其中解释了一些算法。

将 FPV 添加到这个系统中可能会很有趣，可以从无人机的角度看地图算法是如何执行的。就因为它很棒。FPV 也是黑客入侵的沃土:我们特别喜欢这个 [FPV 追踪器，它可以自己旋转以获得最佳信号](https://hackaday.com/2018/05/04/super-simple-super-cheap-fpv-drone-tracking/)，还有这个[使用两个摄像头的 3D FPV 设置](https://hackaday.com/2018/04/21/3d-drone-video/)。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)