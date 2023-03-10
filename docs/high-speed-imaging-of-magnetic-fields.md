# 磁场的高速成像

> 原文：<https://hackaday.com/2018/02/15/high-speed-imaging-of-magnetic-fields/>

在试验核磁共振成像设备和建造自己的 CT 扫描仪之前，彼得·詹森希望将磁场可视化。他的一个小型副业项目是建造三色编码器——可以对一切进行成像的口袋传感器套件——在他的 Roddenberry 认可的工具上玩了一圈磁力计功能后，他决定他必须有一种方法来可视化磁场。经过一些工作后，[他有了每秒数千帧的工具。这是一台磁场摄像机，突破了磁成像技术和“摄像机”一词的定义。](https://hackaday.io/project/18518-iteration-8/log/91551-a-third-high-speed-magnetic-imager-tile)

当我们最后一次查看[Peter]的霍尔效应相机时，该设备工作正常，但不一定完整。最初的设计使用 I2C I/O 复用器来寻址霍尔效应阵列的每个单独的“像素”，将“摄像机”的“帧速率”限制在 30 赫兹左右。虽然这将有助于可视化静态磁场，但我们周围更有趣的磁场是振荡的——想想电机和变压器之类的。需要一个更快的磁相机，这就是[彼得]着手建造的。

[Peter]重新设计了他的设计，不再使用 I/O 扩展器，而是使用模拟多路复用器和二进制计数器来循环每个像素，一次一个像素。基本上，新电路使用两个模拟多路复用器用于霍尔效应阵列的列和行，一个二进制计数器以兆赫的速度循环通过每个像素，一个快速 ADC 读取每个值。奇怪的是，这是 20 世纪 70 年代的做事方式；这些都是简单的芯片，控制器(a Chipkit Max32)只需要读取一个模拟值，并以极快的速度为二进制计数器计时。

通过新的设计，[Peter]能够获得大约 2000Hz 的极快帧速率。对于旋转电机和变压器的一些美丽的可视化来说，这已经足够快了，见下面的视频。进一步的改进可能包括三轴磁力计，这应该允许一些类似于[【Ted Yapo】的 3D 磁场扫描仪](https://hackaday.io/project/11865-3d-magnetic-field-scanner)的壮观可视化。

 [https://www.youtube.com/embed/vxOuoWygxy0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/vxOuoWygxy0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

