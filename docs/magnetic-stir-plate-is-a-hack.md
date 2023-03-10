# 磁力搅拌板是一个黑客

> 原文：<https://hackaday.com/2017/03/08/magnetic-stir-plate-is-a-hack/>

如果你曾经在实验室呆过一段时间，你肯定见过一种令人敬畏的磁力搅拌器和加热板的组合，科学家用它来混合液体并达到温度。如果你曾经用过硫酸铵蚀刻过你自己的 PCB，你就亲身体验过加热和搅拌的需要。使用搅拌板进行 PCB 蚀刻是将两个和两个放在一起，得出四个。也就是说，这是一个不太新奇的好主意。虽然[酸波旁]自己做了一个，但是这个 DIY 加热器/搅拌器几乎没有一个部分不是这样或那样的。

从温度控制器开始。酸波旁没有购买热电偶或使用 LM75 或类似的温度测量 IC，而是使用 bog 标准的 1n4148 二极管。在给定电压下，流过二极管的电流与温度有关，这意味着增加一个电阻和一个微控制器的 ADC 就可以快速侵入温度传感器。[酸波旁]把他的直板粘到他用作蚀刻托盘的砂锅上。

使用二极管而不是温度传感器节省 0.25 美元的人会出去买搅拌器电机吗？不会吧。马达和齿轮来自光盘驱动器。“鱼”——在蚀刻剂中旋转的磁棒——由钕磁铁制成，通过~~热缩包装~~将它们与一些电容器热缩在一起而加长。谁知道~~收缩包装~~热缩，用钳子熔合，是防水的？盒子里的是壁式电源插座吗？

无论如何，这只是表明蚀刻设备不需要昂贵或花哨。这个项目也为一群小黑客提供了展示的机会。说到[酸波旁]的项目，[这个半自动钻床模型](http://hackaday.com/2015/02/04/semi-auto-pcb-drill-press-makes-drilling-semi-painless/)已经在我们的待办事项清单上两年了。为我们感到羞耻！

 [https://www.youtube.com/embed/PtoCuP9K96I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/PtoCuP9K96I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

