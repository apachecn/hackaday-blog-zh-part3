# ESP32 迷你机器人包传感器和 4WD

> 原文：<https://hackaday.com/2017/06/16/esp32-mini-robot-packs-sensors-and-4wd/>

[Stefan]的[迷你 WiFi/BLE 四轮驱动机器人平台](https://hackaday.io/project/25430-mini-wifible-4wd-robot-platform)(见上图火柴盒旁边)将一项令人印象深刻的功能打包到了一辆微型漫游车中。它基于 SparkFun ESP32 的东西，这是一种非常简洁的方式来将无线控制添加到您的项目中。将其与一些带有 WiFi 屏蔽的巨型旧 UNO 进行比较，这些板很小但功能强大，也很容易被 Arduino 粉丝采用。

[Stefan]用 BNO055 模块增强了机器人，以确定方向，一个 APDS-9930 接近传感器，以及底部的四个 CNY70 IR 接近传感器，用于循线。一对 6 V 电机驱动机器人，DC-DC 升压转换器将 LiPo 的 3.7 V 电压升压。令人印象深刻的是，外壳中塞满了多少组件；它们都被紧紧地包在里面。

机器人背后的概念是，它是一个通用平台，可以根据需要进行定制，而[Stefan]有带乐高镖枪和摄像头的版本。机器人的代码位于 GitHub 上，定制的 3D 打印底盘位于 Thingiverse 上。

如果你喜欢 ESP32 项目，你一定要看看我们最近发布的[怪物图板](http://hackaday.com/2017/05/28/esp32-monster-and-getting-started-quickly/)和[仓鼠跟踪器](http://hackaday.com/2017/05/27/esp32-hamster-wheel-tracker-tweets-workout-stats/)。