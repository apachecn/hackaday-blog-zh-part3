# 黑客 86-延时项目

> 原文：<https://hackaday.com/2015/11/28/hacklet-86-time-lapse-projects/>

“如果我能把时间保存在瓶子里……”这不仅仅是一首老歌，这是许多摄影黑客的激情所在。延时摄影是一种通过静止图像展示时间运动的方式。这些图像被制成动画，实质上是以超低帧速率录制的视频。我们说的是每分钟一帧或者在某些情况下更慢！对于这一切，摄像机不必静止，但任何运动都必须小心控制。这导致黑客、制造商和工程师创造了无数的延时装置。本周的 Hacklet 是关于 [Hackaday.io](https://hackaday.io) 上的一些最好的延时项目！

[![rig-1](img/e6ca41639f54e4598998d85d6bd4530e.png)](https://hackaday.io/project/1909) 我们从【Swisswilson】和简单命名的[定时拍摄装置](https://hackaday.io/project/1909)开始。说这个钻机是结实的将是轻描淡写。除了齿轮，所有的铝零件都是由[Swisswilson]加工的。两个 ~~Nema-23~~ Nema-17 电机由 Sparkfun Easy 步进驱动板控制，同时一个 Arduino Micro 充当控制器。所有的电子设备都装在一个坚固的盒子里，这个盒子还可以用作遥控器。操纵杆允许手动控制平移和倾斜。防弹结构无疑是一个帮助，因为[瑞士威尔逊]正在使用这个钻机与 DSLR 相机。结合一个镜头，这些装置可以达到一两磅。

[![pilapse](img/a76e2205ff800f315fc95ea5d00a7b52.png)](https://hackaday.io/project/4266) 下一个是【明维】，他把他们的脚本 foo 和[拉斯皮拉斯](https://hackaday.io/project/4266)一起工作。Raspilapse 将拍摄照片、将照片组装成电影以及上传到 YouTube 的整个过程自动化。硬件是 Raspberry Pi 型号 B，带 RasPi 摄像头。Pi 拍摄图像，然后将它们上传到虚拟专用服务器(VPS)。[minWi]使用外部服务器来减少 Pi 的 SD 存储卡的磨损。在一天结束时，VPS 使用 ffmpeg 将图像组合成视频，然后将整个内容上传到 YouTube。我们打赌，通过一些脚本模块，整个过程可以在 Raspberry Pi 2 上运行。如果你真的担心 SD 卡，可以使用 u 盘。

[![SunriseSunsetRig](img/4394262a869ff4036c6110cbacb0b86b.png)](https://hackaday.io/project/2126) 【安迪哈尔】用[日落日出相机控制器](https://hackaday.io/project/2126)把我们带到每天一帧。[安迪]想拍下每天的日出。一旦转换成视频，这些镜头对于记录季节的流逝是非常棒的。他用佳能的傻瓜相机和佳能的套件(CHDK)来装他的相机。相机有自己的实时时钟，通过 CHDK，它可以被编程为在日出时拍摄图像。问题是权力。让相机一直开着会很快耗尽电池。Arduino 来救援了！[Andy]给 Arduino Pro Mini 编了一个程序，让它在日出前打开摄像头，然后再关闭。休眠的 ATmega328 的待机功率比相机低得多，导致电池寿命以周计。

[![pod](img/6521d9a546e2f012b18baa1bc6c87f9c.png)](https://hackaday.io/project/4432) 最后，我们有【caramellcube】他们用[便携式观测设备(POD)](https://hackaday.io/project/4432) 给自己的延时照片添加数据。POD 被认为是一种帮助超自然现象调查者的设备。这个想法是有一个设备，可以在一个锁着的房间里以设定的时间间隔拍摄图像和记录数据。听起来像是树莓派的工作！[caramel cube]从 Adafruit 基于 Raspberry Pi 的触摸屏相机套件开始。从那里，他们添加了由 Arduino Nano 控制的第二块电路板。Nano 几乎可以读取[caramel cube]可以安装的所有传感器，包括湿度、气压、磁场强度、加速度、光线(4 个波段)、声音和静电荷。Nano 允许[caramel cube]通过 Pi 上的一个 USB 端口连接所有这些传感器。我们不确定[caramel cube]是否发现了任何鬼魂，但我们确信我们的读者可以想到这样一个设备的许多用途！

如果你想看更多的延时项目，请查看我们新的[延时项目列表](https://hackaday.io/list/8597-time-lapse-projects)！如果我错过了你的项目，不要害羞，只要[在 Hackaday.io](https://hackaday.io/adam) 上给我留言。这就是本周的 Hacklet。一如既往，下周见。同样的黑客时间，同样的黑客频道，带给你最好的 [Hackaday.io](https://hackaday.io/) ！