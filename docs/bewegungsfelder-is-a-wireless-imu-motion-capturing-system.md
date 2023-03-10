# Bewegungsfelder 是一个无线 IMU 运动捕捉系统

> 原文：<https://hackaday.com/2016/09/13/bewegungsfelder-is-a-wireless-imu-motion-capturing-system/>

几年来，黑客一直在探索惯性测量单元(IMU)作为廉价的[传感器，用于运动捕捉](http://hackaday.com/2013/08/15/imu-boards-as-next-gen-motion-capture-suit/)。[Ivo Herzig 的]最终文凭项目[“Bewegungsfelder”将基于 IMU 的 MoCap 概念又向前推进了一步](http://herrzig.ch/work/bewegungsfelder/)，它采用了基于捆绑式、支持 WiFi 的 IMU 模块的可自由配置的动作捕捉系统。

Bewegungsfelder 系统由多个 ESP8266 供电的独立 IMU 传感器节点和一个运动捕捉服务器组成。这些节点附着在人体(或其他任何物体)上，将板载 MPU6050 6 轴加速度计/陀螺仪的输出无线传输到中央运动捕捉服务器。服务器应用程序将输入的数据转换成骨架动画，将它们可视化为实时预览，并存储 MoCap 数据以备后用。由于传感器节点是完全独立的，它们可以很容易地重新配置成任何骨骼拓扑结构，无论是人、猫还是工业机器人。

[![robocap](img/a02535a1e2fef57d4081e712d9a02767.png)](https://hackaday.com/wp-content/uploads/2016/09/robocap.gif)

[Ivo]已经包括对自定义骨架定义的支持，以及 BVH 导入/导出，以便在常用工具(如 Maya 的 Blender)中使用生成的数据。该项目的软件部分在 MIT 许可下作为开源发布，GitHub 上提供了[固件和服务器应用代码](https://github.com/herzig/bewegungsfelder)。根据[Ivo]的说法，这些节点可以以低至 5 美元的价格建造，这使它们在 AR/VR 应用程序中处于一个不错的价格范围内——或者用于制作你的[自己的漫画](http://hackaday.com/2016/01/23/amazing-imu-based-motion-capture-suit-turns-you-into-a-cartoon/)。

[![mocap-opti](img/ead6b1ba0ac3ba4c255ff8fe43b7aad4.png)](https://hackaday.com/wp-content/uploads/2016/09/mocap-opti1.gif)