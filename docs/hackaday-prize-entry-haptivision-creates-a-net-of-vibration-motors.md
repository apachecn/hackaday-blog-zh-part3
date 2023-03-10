# Hackaday 奖参赛作品:HaptiVision 创造了一个振动马达网络

> 原文：<https://hackaday.com/2017/09/22/hackaday-prize-entry-haptivision-creates-a-net-of-vibration-motors/>

[HaptiVision](https://hackaday.io/project/27112-haptivision) 是一款为盲人设计的触觉反馈系统，它建立在一系列振动带和触觉背心的基础上。这是一个聪明的概念，当障碍物进入传感器视野时，会向佩戴者发出警告。

对触觉反馈可穿戴设备的最早研究使用了超声波传感器，最近的开发使用了 Kinect。HaptiVision 的项目团队选择了英特尔实感摄像头，因为它的外形纤薄。目标的一部分是使触觉尽可能的谨慎，所以将整个装置安装在衬衫下是计划的一部分。

除了一个 RealSense 摄像头，该团队还为大脑使用了一个英特尔[主板](http://www.up-board.org/upsquared/)，主要是因为它本来就可以控制 RealSense 摄像头。它可以拍摄 640×480 的红外快照，并选择性地触发 128 个振动马达来告诉你什么在附近。电机由 8 个基于 PCA9685 的 PWM 扩展板控制。

该项目基于 David Antón Sánchez 的 [OpenVNAVI 项目](http://hci.rwth-aachen.de/openvnavi)，该项目也采用了 128 电机阵列。HaptiVision 旨在创建一个易于复制的触觉系统。一切都是开源的，所有的接线夹和电机支架都是 3D 打印的。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)