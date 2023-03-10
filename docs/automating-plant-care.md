# 自动化植物护理

> 原文：<https://hackaday.com/2017/07/11/automating-plant-care/>

[Daniyal]的目标是建造一个自动化花园，让他可以在任何他选择的环境中种植植物。他在这个装备上有一个良好的开端，它由一个 Pi Zero 通过串行连接到 Arduino Mega clone 来控制，Arduino Mega clone 反过来控制一组继电器和传感器。

监测环境的是一个温度和湿度传感器以及一系列的六个土壤湿度传感器钉。继电器控制水泵。)和灯光，让[Daniyal]根据自己种植的作物保持特定的条件。

[Daniyal]对这个项目有着雄心勃勃的目标。Pi 上面有一个摄像头，他希望不仅可以从互联网上维护温室，还可以想出如何自动监控植物生长，这样 Pi 就可以在没有他的输入的情况下测量植物生长并调整条件。

我们已经在 HaD 上报道了很多非常酷的园艺项目，包括[无线电连接土壤传感器](http://hackaday.com/2017/03/03/using-backscatter-radio-for-a-soil-sensor-network/)，使用 G-cal 创建[草坪互联网](http://hackaday.com/2017/04/13/google-calendar-interface-for-your-internet-of-lawns/)，以及[伊甸园浇水套件](http://hackaday.com/2016/10/01/hackaday-prize-entry-the-geck/)。