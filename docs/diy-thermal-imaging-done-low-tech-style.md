# 低技术风格的 DIY 热成像

> 原文：<https://hackaday.com/2017/01/19/diy-thermal-imaging-done-low-tech-style/>

[Niklas Roy]一直想尝试热成像，当他收到一个手持红外温度计作为礼物时，他看到了自己的机会。但他并不满足于仅仅将它指向不同的点并在 LCD 显示屏上查看温度，他决定将它用作扫描热成像系统的基础，该系统将在他的笔记本电脑上显示一个选定位置的热图。

![DIY thermal imaging system](img/5eeb8c258d6acb119432ade3ca9e0517.png)

DIY thermal imaging system

他仍然希望能够在以后正常使用红外温度计，所以切开它不是一个选项。相反，他坚定地安装了一个摄像头，指向液晶显示器。然后，他在自己的笔记本电脑上编写了软件来处理生成的图像，并计算出显示的温度。

一旦他让温度计工作，他接下来将温度计放在一个平台上，伺服系统连接到 Arduino，用于在水平和垂直方向上缓慢旋转温度计，也是在笔记本电脑上的软件控制下。每当温度计测量一个点的温度时，软件就会解码 LCD 显示屏上的温度，然后告诉 Arduino 使用伺服系统将温度计指向下一个待测点。每次测量需要一点时间，因此扫描 70×44 个点的整个位置需要大约半个小时。但是最终的结果是一张绘制在笔记本电脑上的热图，是由一个低技术含量的设备完成的。[编者的话:因为如今安装网络摄像头和处理图像是“低技术含量”的。]他可以将热图叠加在普通照片上，一眼就能看出热点在哪里。

他写的软件可以在 GitHub 上获得，下面的视频展示了它的运行。我们不得不承认，这看起来很棒。您甚至可以看到热图一次填充一个度量。

[Niklas]在某种程度上是 Hackaday 的常客，他的项目涵盖了一系列令人印象深刻的创意。看看他的[大型音乐建造机](http://hackaday.com/2016/07/05/niklas-roys-music-construction-machine/)，或者他的 [RC 啤酒箱运送机器人](http://hackaday.com/2016/06/07/rc-beer-crate-handles-rough-terrain-like-a-pro/)，或者他的[超大 DIY 弹球机](http://hackaday.com/2015/06/05/galactic-dimension-a-supersized-diy-pinball-machine/)。无论你做什么[Niklas]，保持那些创造性的汁液流动！

 [https://www.youtube.com/embed/q49p4jXGQuA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/q49p4jXGQuA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

