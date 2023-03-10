# IPhone 偏光相机使用闪光灯解决滤镜方向问题

> 原文：<https://hackaday.com/2016/07/04/iphone-polarizing-camera-solves-filter-orientation-problem-using-flash/>

去年的 Hackaday 奖决赛选手之一是 DOLPi，[Dave Prutchi]的偏振相机，它使用了一个焊工面罩上的 LCD 片，放在树莓 Pi 相机前面。DOLPi 以不同的偏振拍摄了多幅图像，并用于计算图像，这些图像旨在显示每个像素中的光偏振，并通过颜色将其传达给观众。

[![The polarizer and phototransistor taped to the iPhone.](img/12fea2486edf7a2a7a0c3fd570a0b013.png)](https://hackaday.com/wp-content/uploads/2016/07/head-detail.jpg)

The polarizer and phototransistor taped to the iPhone.

[Dave]写信告诉我们[Paul Wallace]也有同样的想法，这是一款受 DOLPi 启发的偏振相机，使用 iPhone 巧妙解决了将设备校准到每张图像的正确偏振角度的问题，不需要手机和相机硬件之间的任何电气连接。[Paul]的相机是使用 iPhone 的闪光灯校准的。通过 LCD 的闪光灯发出的光由光电晶体管和 Arduino Mini 测量，Arduino Mini 将 LCD 设置为正确的偏振。整个装置被贴在 iPhone 的背面，尽管我们怀疑 3D 打印的支架不会有太多问题。他在博客上提供了控制相机和计算图像的 iPhone 应用程序的全部细节和代码。

去年我们[详细报道了 DOLPi](https://hackaday.com/2015/07/28/polarization-camera-views-the-invisible/)，作为我们 [2015 年 Hackaday 奖决赛选手](https://hackaday.io/list/7999-2015-hackaday-prize-finalists)报道的一部分。你还可以在 Hackaday.io 上找到[的页面，以及](https://hackaday.io/project/6958-dolpi-raspi-polarization-camera)[【戴夫】自己在博客](http://uvirimaging.com/2016/07/02/dolpi-ui-a-diy-uvirpolarization-imager/)上的评论。