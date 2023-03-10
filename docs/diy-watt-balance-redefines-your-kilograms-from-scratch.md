# DIY 瓦特秤从零开始重新定义您的千克

> 原文：<https://hackaday.com/2016/09/30/diy-watt-balance-redefines-your-kilograms-from-scratch/>

[![national_prototype_kilogram_k20_replica](img/fc6ef152f4dc05be29412cc7bc6b6d1f.png)](https://hackaday.com/wp-content/uploads/2016/09/national_prototype_kilogram_k20_replica.jpg)

The definition of the kilogram is still a chunk of metal.

国际原型千克(IPK)由一大块几乎坚不可摧的铂铱合金加工而成，可以永久使用。然而，作为基本 SI 单位俱乐部中最后剩下的物理人工制品，千克的当前定义已经过时了。毫无疑问，瓦特秤将取代它的位置，用真实的物理现象重新定义千克。[格雷迪]刚刚从零开始建造了他自己的瓦特秤，他为你提供了关于这个问题的科学背景的[体面部分。](http://practical.engineering/blog/2016/9/25/redefining-the-kilogram-desktop-watt-balance)

瓦特秤的外观或操作与普通天平没有太大区别，只是瓦特秤采用了校准的电磁反作用力，而不是用校准的配重称量未知质量。该力由电磁致动器产生。[Grady]scratch-build 他的瓦特平衡木材，然而，即使他小心翼翼地转动和缠绕自己的电磁铁线圈，他也不能十分确定他的驱动器每安培消耗电流所施加的力的确切大小。在重新定义瓦特秤的重量(公斤)之前，这个新装置需要校准。

 [![Turning the spools](img/f8e4cdb5629b81d617915ccab4c34cbd.png "vlcsnap-2016-09-28-15h45m43s451")](https://hackaday.com/2016/09/30/diy-watt-balance-redefines-your-kilograms-from-scratch/vlcsnap-2016-09-28-15h45m43s451/) Turning the spools [![Winding the coils](img/494777b29217b418c47f51ad8da396b5.png "vlcsnap-2016-09-28-15h43m15s235")](https://hackaday.com/2016/09/30/diy-watt-balance-redefines-your-kilograms-from-scratch/vlcsnap-2016-09-28-15h43m15s235/) Winding the coils [![The shadow sensor](img/08502273397ac275a43bce510bbd5fd9.png "vlcsnap-2016-09-28-15h28m35s967")](https://hackaday.com/2016/09/30/diy-watt-balance-redefines-your-kilograms-from-scratch/vlcsnap-2016-09-28-15h28m35s967/) The shadow sensor

由于代数和物理学，这可以通过测量电磁致动器自身在外力作用下以给定速度移动其永磁芯时产生的电压来实现。因此，watt-balance 配备了第二个电磁致动器，带有光学位置反馈(实际上是一个伺服系统)，可以轻微地来回摇动天平。[Grady]通过在天平的臂上安装一个由线激光器和光电二极管组成的阴影传感器，实现了光学反馈。Arduino Uno 轮询传感器，对感应电压进行采样，并将测量数据发送到[Grady 的]主机软件。在此*速度模式*下校准后，天平在其*称重模式*下运行，在此模式下，通过简单调整流经电磁铁线圈的电流，所述质量的重力和致动器施加的电磁力达到平衡。

我们很高兴看到这些[巨大的仪器](https://www.nist.gov/pml/redefining-kilogram-watt-balance)是用木头或者[甚至乐高](https://hackaday.com/2015/01/08/measuring-the-plank-constant-with-lego/)建造的。请欣赏下面的视频，其中[Grady]带您了解他的瓦特秤背后的工程技术。

 [https://www.youtube.com/embed/ewQkE8t0xgQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ewQkE8t0xgQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

