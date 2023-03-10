# 使用 IMU 进行里程计测量

> 原文：<https://hackaday.com/2018/06/17/using-imus-for-odometry/>

未来是自主机器人。无论这意味着具有更名的自适应巡航控制的电动汽车，还是实际上只是遥控汽车的送货机器人，未来的机器人都需要决定如何移动，向哪里移动，并能够跟踪自己的移动。这就是里程计的问题，或者说机器人走了多远。有很多方法可以解决这个问题，但 GPS 不够精确，在车轮上安装编码器也不能解释打滑。机器人里程计真正需要的是多个传感器，为此我们有[Pablo]和[Alfonso]的 Hackaday 奖的参赛作品，[录像机](https://hackaday.io/project/158496-imcoders)。

IMcorder 是一款简单的设备，装载了一个 MPU9250 IMU 模块，该模块集成了加速度计、陀螺仪和指南针。它连接到 Arduino Pro Mini 和蓝牙模块，允许 IMcorder 与机器人的主计算机通信，以提供机器人的方向和加速度信息。所有这些都放在一个带有锂电池的非常小的 PCB 上，允许这个项目集成到任何机器人项目中，而无需太多修改。

录像机的一个有趣的方面是，它们可以用于机器人绑架问题。当机器人和其他电子垃圾在人行道上乱扔时，这显然是一个问题。那些被遗弃在几个城市人行道上的电动滑板车包含一些令人惊讶的组件，这些组件对于一些伟大的硬件黑客来说已经成熟。最终，我们将会看到一些关于人们为了自己的个人使用而偷窃滑板车和送货机器人的新闻报道。是的，这是一个赛博朋克的梦想，但录像机可以用于一点点的防盗。很遗憾。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)