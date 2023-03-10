# 在 26 个不同的方向拍摄视频

> 原文：<https://hackaday.com/2017/05/31/shoot-video-in-26-different-directions/>

[马克·穆林斯]正在从事一个名为 Quamera 的项目:一种能够同时从各个方向拍摄视频的相机，能够实时创建 3D 环境。

[Mark]正在使用 26 个 Arducams，将它们排列成菱形八面体结构，该结构由 8 个摄像机组成的三个环组成，每个环由一个 Beaglebone 控制；顶部和底部的圆环成 45 度角，而中间的圆环看起来是直的。顶部和底部的摄像头由第四个 Beaglebone 控制，它也用于与运行一切的 Nvidia Jetson TX1 通信。总之，这些相机可以同时看到所有方向，有足够的重叠为观众提供无缝显示。

[![](img/e431ff19dd4910276e8f85a7e0465793.png)](https://hackaday.com/wp-content/uploads/2017/05/quamera2.png) 在右边的图片中，【马克】正在测试他的软件，让各种摄像机协同工作。圆圈的银行和连接它们的点和线代表了计算机对如何无缝合并图像的最佳猜测。

如果你想亲自看看这个项目，[马克]将会在今年八月的多佛小型制造商博览会上展示这款相机。与此同时，要了解更多关于杰特森的信息，请查看我们的[对董事会的全面概述](http://hackaday.com/2015/11/24/the-nvidia-jetson-tx1-its-not-for-everybody-but-it-is-very-cool/)。