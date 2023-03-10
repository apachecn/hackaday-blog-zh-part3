# 廉价的双面镜激光投影仪

> 原文：<https://hackaday.com/2016/11/23/cheap-dual-mirror-laser-projector/>

[斯坦利]想做一个激光投影仪，但他在网上只能找到一个使用昂贵的振镜扫描仪。因此，他想出了自己的解决方案，该方案因其简单性和对他所能找到的内容的适应性而令人钦佩。

它的核心是 Arduino Uno 和 Adafruit Motor Shield v2。Arduino 通过一个晶体管打开和关闭绿色激光器。但是让这台机器看起来很有趣的部分是两个步进电机和两个在 X 和 Y 方向反射激光的镜子。镜子是从硬盘上切割下来的长方形，如果你见过的话，它非常反光。伺服系统使镜子高速倾斜，快得足以根据图像使墙上的投影看起来几乎是实心的。

他甚至编写了一个 Windows 应用程序(用 C#)来通过蓝牙远程控制投影仪。在它的界面上，你可以从大约 16 种预定义的形状中进行选择，包括一个看起来像猫头的形状、一颗心、一个人以及各种几何物体和线条配置。

在图像由形成一个角度的两条线组成的地方，线有一种弯曲，好像步进器在动量上有问题，但这可能是预期的，因为它们是控制相对较大的镜子的步进器。或者可能是由于电机轴和镜子之间的连接扭曲？休息之后看看视频，让我们知道你的想法。

该视频分为三个部分:观看活动中的激光束，就像你在舞池中看到它们一样，然后观看投影图像，同时观看 Windows 应用程序的插件，然后观看步进器和镜子快速移动。

至于我们上面提到的昂贵的检流计扫描仪，看看这个令人印象深刻的使用它们的激光投影仪。另一种方法是使用一个旋转的轮子，镜子设置在不同的角度，就像这个[用一个药丸盒作为轮子](http://hackaday.com/2010/09/15/laser-marquee-projector/)来画一个选取框。还有一个完全没有镜子，而是[将激光直接连接到伺服电机](http://hackaday.com/2013/11/24/hack-a-day-logo-laser-light-show/)上的怎么样，尽管那个需要更长的时间来绘制。

 [https://www.youtube.com/embed/zM5dDZWUGso?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zM5dDZWUGso?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

