# hacklet 97–相机项目

> 原文：<https://hackaday.com/2016/02/26/hacklet-97-camera-projects/>

我们上次讨论相机项目要追溯到 Hacklet #11。从那以后，大量的相机项目被添加到了 Hackaday.io。当世界其他地方都在自拍时，黑客、制造商和工程师们已经想出了新的方法来侵入他们的图像捕捉设备。本周在 Hacklet 上，我们来看看 Hackaday.io 上一些最好的相机项目！

[![pixelz](img/2a604f3668fa32ef74846733c9f34d28.png)](https://hackaday.io/project/9866) 首先出场的是【aleksey.grishchenko】与[像素摄像头](https://hackaday.io/project/9866)。PiXel 集相机和实时视频显示于一身，但我们不能称之为高清！树莓派用它的相机模块捕捉世界的图像。[Aleksey]然后处理这些图像，并在 32 x 32 RGB LED 矩阵上显示它们。这种矩阵与大型户外 LED 标志中使用的瓷砖类型相同。结果是一个超现实的低分辨率的世界。由于 Pi、电池和摄像头都隐藏在 LED 矩阵后面，因此您周围的世界一览无余。[Aleksey]使用[Henner Zeller 的] [矩阵库](https://github.com/hzeller/rpi-rgb-led-matrix/)来实现这种攻击。

[![imager](img/5b581e51c15ba3b937866907500525d6.png)](https://hackaday.io/project/9829) 接下来是【埃斯本·罗塞尔】带[线阵 CCD 模块](https://hackaday.io/project/9829)。[Esben]正在建造一台拉曼光谱仪，很像 2014 年 Hackaday 奖决赛选手[fl@C@]用他自己的 [ramanPi](https://hackaday.io/project/1279) 。光谱仪的核心是线性图像捕捉设备。这两个项目都使用相同的 TCD1304 线性 CCD。线性电荷耦合器件(CCD)与平板文档扫描仪中使用的设备类型相同。CCD 的输出是模拟信号，因此必须使用 ADC 来采集数据。[Esben]使用 Nucleo 板上的 STM32F401RE 作为控制逻辑。ST 的内部 ADC 将模拟信号转换为数字信号。从那里，是时候处理所有的光谱了。

[![wiimote-cam](img/9eef359c53a04fbb4afa6a0492c489ae.png)](https://hackaday.io/project/9830)【chip robot】用
[ESP8266 遇上 Wii Mote Camera](https://hackaday.io/project/9830) 将经典的 Wii 远程相机带入物联网。Wii 遥控器使用一个不输出图像的摄像头，而是绘制多达四个红外 led 的位置。通常情况下，这些发光二极管位于 Wii 出售的传感器条上，但这个传感器条的名字并不响亮。黑客已经在项目中使用这些相机多年了。[Chiprobot]将他的相机与现代经典的 ESP8266 WiFi 模块配对。8266 被编程为从摄像机的 I2C 总线读取数据。然后，它将数据作为 SVG 请求发送到 W3C 网站。W3C 返回基于这些坐标的格式化图像。生成的图像是相机看到的红外发光二极管的图片。有点像把你的底片送去冲洗。

[![photobooth](img/53b90c707f7537913be5ae98b16254a4.png)](https://hackaday.io/project/6625) 最后，我们有【古意斯特】与[树莓派照相亭](https://hackaday.io/project/6625)。如今照相亭风靡一时。一开始是婚礼，但现在好像每个儿童派对都有。[GuyisIT]没有为他女儿的生日租一个摊位，他用他的树莓 Pi 和 Pi 相机做了一个。该项目是用 python 编写的，基于[【John Croucher 的】代码](https://github.com/jcroucher/pi-photo-booth/blob/master/photobooth.py)。当孩子们按下一个按钮时，私家侦探会拍下一系列照片。微型 Linux 计算机然后连接和旋转图像，同时添加一些超级英雄主题的图形。最后，Pi 将图像打印到照片打印机上。这种黑客最大的问题是重新触发。孩子们非常喜欢它，他们不停地按红色的大按钮！

如果你想看到更多的相机项目，请查看我们的[更新相机项目列表](https://hackaday.io/list/2643-cameras)！如果我错过了你的项目，不要害羞！就[在 Hackaday.io 上给我留言](https://hackaday.io/adam)。这就是本周的 Hacklet。一如既往，下周见。同样的黑客时间，同样的黑客频道，带给你最好的 [Hackaday.io](https://hackaday.io) ！