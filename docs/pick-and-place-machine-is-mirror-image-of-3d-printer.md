# 拾放机是 3D 打印机的镜像

> 原文：<https://hackaday.com/2018/05/11/pick-and-place-machine-is-mirror-image-of-3d-printer/>

为了他的 Hackaday 奖参赛作品，[Daren Schwenke]正在为一台 3D 打印机创造一个[开源的拾放头，它本身基本上是 3D 可打印的。一些严重的肘油脂已经进入这个设计，它显示。](https://hackaday.io/project/45404-arcus-3d-p1-pick-and-place-for-3d-printers)

这个项目真正精彩的部分在于对被放置的零件的成像。目的是在零件移动时，使用一系列在头部下方摆动的镜子对其进行成像。Raspberry Pi 相机用于拍摄照片，LED 光晕提供一致的照明，虽然看起来像是 [OpenPnP](http://openpnp.org/) 可能需要稍微修改才能完成，但它肯定会令人印象深刻。

![](img/7aa6297e9f76117d41e493c1972401c2.png)

使用了两个 9g 业余伺服系统:一个用于摆动镜子(耗时 0.19 秒)，一个用于将零件旋转到正确的方向(齿轮比为 2:1，允许 360 度零件旋转)。整个头部重 59 克，比 E3D v6 发动机还轻。

为了让这个项目达到目前的状态，[达人]不得不进行一些辅助性的修改。第一个是[水族馆到真空泵的转换](https://hackaday.io/project/45998-p1-aquarium-to-vacuum-pump-conversion)——通过切换阀门和执行一些其他小的修改，[达人]能够产生 231 毫巴的真空。第二个是[将咖啡机的一个双向电磁阀](https://hackaday.io/project/40381-p1-solenoid-3-way-conversion)改装成一个三通装置。正如[达人]所说，三通阀并不贵，但“在阿里巴巴上，一个在手的零件抵得上两个。”

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)