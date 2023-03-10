# 老式缝纫机到电脑绣花机

> 原文：<https://hackaday.com/2018/02/21/vintage-sewing-machine-to-computerized-embroidery-machine/>

现在是 2018 年 2 月。你记得 2012 年 12 月你在做什么吗？如果你是(juppiter)，你正在启动你的[数控刺绣机](http://boxedcnc.blogspot.it/2018/02/embroidery-cnc-first-completed-work.html)，它在五年多的时间里都不会完成。结果不言自明，但这可能是我们最后一次看到第一代树莓派而不称其为复古。

建筑的核心是一台老式的 Borletti 缝纫机，如果你喜欢机械色情，你会在休息后欣赏视频。机器的大脑是一个充满 GRBL 善良的 Arduino UNO 和运行 CherryPy 的 Pi。对于肌肉，有三个 Postep25 步进驱动器和相应的 NEMA 17 步进电机。

![](img/64c394a1d763263a7997fbd8c5d142fe.png)

前两个轴用于 X-Y 工作台，负责移动织物通过机器。第三个轴是飞轮。织物框架的刚性来自其黄铜结构，这可能是在厨房餐桌上焊接的，并由一只橙色的大猫监督。刚性框架是获得可靠结果的第一要素，但皮带张力不可低估。他的[皮带张紧技巧](http://boxedcnc.blogspot.it/2013/06/cnc-embroidery-la-base-in-legno-parte.html)对你来说可能并不陌生，但对我们中的一些人来说却是新的。意大利语翻译可能是必要的。

为这一构建汇集的技能是巨大的。有结构焊接、零件加工、微控制器和运动控制。我们第一次听到来自[juppiter]的消息是在 2012 年 12 月，这是一个[便携式数控铣床](http://hackaday.com/2012/12/28/a-portable-cnc-mill/)的结果，它可能对这个创作有一些影响。从那以后，他还和我们分享了他的[四分之一大的街机柜](http://hackaday.com/2016/10/09/arcade-cabinet-build-takes-quarters-dispenses-fun/)。

 [https://www.youtube.com/embed/voy9yxcEz38?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/voy9yxcEz38?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

