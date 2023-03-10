# Hackaday 奖参赛作品:廉价、开放的激光雷达

> 原文：<https://hackaday.com/2016/07/05/hackaday-prize-entry-cheap-open-lidar/>

[亚当]是一个洞穴探险者，意思是他喜欢探索洞穴并绘制其内部结构。这仍然通常使用传统工具来完成，例如笔记本(纸质的)、卷尺、圆规和测斜仪。[adam]想要升级他的设备，但是发现工业激光雷达 3D 扫描仪相当昂贵。他的 Hackaday 奖参赛作品[开放式激光雷达](https://hackaday.io/project/11598-open-lidar)，是昂贵的工业 3D 扫描解决方案的廉价替代品。

[![The 3D scan of a small cave near Louisville (source: [caver.adam's] Sketchfab repository)](img/1ef5fb9a8c5a5585c3c61ff7d3807076.png)](https://hackaday.com/wp-content/uploads/2016/06/bildschirmfoto-2016-06-27-um-20-02-11.png) 

来自[【caver . Adam’s】sketch fab repository](https://sketchfab.com/models/b94b554192974dd580050849447514d7)

激光雷达——光探测和测距——是一种通过反射测量光束在两者之间的飞行时间来感知传感器和物体之间距离的技术。通过获取多个距离读数的二维阵列，这可以用于 3D 扫描。在观察工业激光雷达扫描仪如何使用快速旋转的镜子捕捉环境时，[adam]意识到他可以通过使用一个绑在云台上的廉价激光测距仪来基本上实现相同的目标。

他为这项任务设计的万向架使用步进电机来瞄准 SF30-B 激光测距仪。Arduino 控制移动，并让传感器的眼睛扫描一个对象或整个环境。通过对传感器返回的距离读数进行采样，可以创建点云，然后将其转换为 3D 模型。[adam]计划以微步模式驱动步进电机，以提高扫描仪的分辨率。我们期待看到用开放式激光雷达拍摄的 3D 洞穴地图的第一张渲染图。

The [HackadayPrize2016](http://hackaday.io/prize) is Sponsored by: [![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](http://hackaday.io/atmel)  [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](http://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](http://www.digikey.com/)  [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](http://supplyframe.com/)