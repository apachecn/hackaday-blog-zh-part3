# 一种负担得起的松下栅眼热成像相机

> 原文：<https://hackaday.com/2016/03/24/an-affordable-panasonic-grid-eye-thermal-imaging-camera/>

热成像相机是各地黑客和制造商渴望的对象，但遗憾的是，对我们来说，它们可能相当昂贵。当你的传感器比一台笔记本电脑还贵时，它就能阻止黑客入侵。

幸运的是，帮助就在眼前，这是一款价格合理的评估板，用于松下栅眼热成像相机传感器。这种传感器之前已经引发了 Hackaday 社区的兴趣，[在 2014 年 Hackaday 奖半决赛的一个项目中出现过，但事实证明极难获得。](https://hackaday.io/project/1389-grid-eye-ble-capable-thermal-camera)

现在，有了这个板，一切都变了。它具有栅眼传感器本身、Atmel ATSAM-D21G18A 微控制器和板载蓝牙，但有一个有趣的功能，即作为独立设备，可以用作 Arduino 屏蔽。提供了完整的 API，代码是 BSD 许可的。

这个模块无论如何都不是市场上最高规格的热成像相机，毕竟它在 8×8 网格中的分辨率只有 64 像素。但是它的可负担性和易获得性应该会在我们的社区中引发一批新的热感相机项目，我们对此表示赞赏。

热感相机项目在 Hackaday 上出现了好几次。有些是基于 FLIR 轻子模块，像[这个将其图像与 640×480 可见相机](http://hackaday.com/2015/12/25/build-your-own-thermal-camera/)和[另一个声称是最小的热感相机之一](http://hackaday.com/2014/09/07/building-the-worlds-smallest-thermal-camera/)，而其他人则利用原始的独创性创造了一个没有传感器阵列的热感相机。[这种云台设计比如说](http://hackaday.com/2013/12/01/diy-thermal-imaging-camera/)，或者[这种光线绘画的巧妙运用](http://hackaday.com/2013/01/03/an-absurdly-clever-thermal-imaging-camera/)。拜托，让他们来吧！

[via [oomlout](http://oomlout.co.uk/blogs/news/93270529-panasonics-affordable-grid-eye-arduino-thermal-camera-board)