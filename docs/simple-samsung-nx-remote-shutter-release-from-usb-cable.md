# 简单的三星 NX 遥控快门释放从 USB 电缆

> 原文：<https://hackaday.com/2016/02/27/simple-samsung-nx-remote-shutter-release-from-usb-cable/>

三星制造了一些不错的相机，但他们陷入了建立专有控制器的陷阱。例如，他们的 NX 型号有一个微型 USB 端口，而不是更常见的 2.5 毫米插座，用于远程触发相机。黑客能做什么？

[Niels]做了一些调查，发现远程触发这些相机非常容易，因为三星只需将快门半按和全按的标准连接移到 USB 插座上:接地 D+(引脚 3)，相机对焦，然后接地 D-(引脚 2)，快门被触发。在他的 Instructable 中，他讲述了如何用一根微型 USB 电缆和几个开关来制作一个简单的遥控器。

如果你有另一种类型的数码相机，不要觉得被排除在外:有很多方法可以用几个简单的部件制造一个简单的快门释放开关，或者用一个 T2 微控制器控制更复杂的拍摄。