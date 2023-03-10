# 终极 FPV 清理房子

> 原文：<https://hackaday.com/2017/02/03/the-ultimate-fpv-cleans-house/>

随着世界大部分地区陷入冬季的低迷，黑客们变得有点疯狂。宁愿在外面驾驶他的第一人称视角(FPV)四轴飞行器。当然有室内无人机，但[注名]想保持接地。他拿起他的遥控设备、他的 Roomba，当然还有一台 Arduino [来打造终极 FPV 体验](https://vimeo.com/129404075)。

这个版本没有太多细节，但是不难推断出[Notamed]做了什么。他用的是标准遥控发射器和接收器。接收器插入 Arduino Uno，而不是驱动伺服系统。Uno 将 PPM R/C 信号转换为串行命令。大多数 Roomba 都包括一个专门为黑客设计的串口。[Notamed]只需发送适当的 iRobot 串行命令接口(SCI)消息，机器人就由他来控制了。

FPV 这边的东西是一个 bog 标准 FPV 相机和发射机，发送标准清晰度视频到他的护目镜。GoPro 可以捕捉高质量的视频。

当然，这是一个快速拼凑的版本。所有部件都粘在 Roomba 上。我们确信这是故意的。当天气变暖时，遥控设备回到空中，Roomba 就变成了另一个吸尘机器人——再一次成为到处乱扔宠物垃圾的危险。

休息之后请看视频。

[https://player.vimeo.com/video/129404075](https://player.vimeo.com/video/129404075)