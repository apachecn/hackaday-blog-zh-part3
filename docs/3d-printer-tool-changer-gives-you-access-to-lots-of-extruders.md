# 3D 打印机换刀装置可让您使用大量挤出机

> 原文：<https://hackaday.com/2017/08/27/3d-printer-tool-changer-gives-you-access-to-lots-of-extruders/>

拥有一台带有多个挤出机的 3D 打印机有很多好处:你可以打印可溶性支撑材料以便于移除，打印柔性和刚性细丝的组合，或者简单地打印不同的颜色。不幸的是，传统的多挤出机装置有一些严重的缺点，即使不考虑成本。

通常，挤出机都并排安装在一个托架上。这会增加质量，从而导致阴影等打印质量问题。它还减少了可印刷区域，因为每个挤出机需要能够到达整个区域。所有这些都意味着每增加一台挤出机，设计就变得越来越不切实际，这就是为什么在一台打印机上看到两台以上挤出机的情况并不常见。

[在 hack aday . io](https://hackaday.io/project/26053-tool-switching-multi-extrusion)上，[rolmie]提出了一个非常实用(而且负担得起)的解决方案来解决这个问题。他设计了一个工具更换器，使打印机能够在运行中切换热端。该系统非常类似于我们在 CNC 加工中心看到的刀具更换器:刀具(刀柄)存储在机架上，g 代码中的刀具更换会将托架发送到机架上，以放下旧刀柄并拿起新刀柄。

这种设计的好处是车厢的质量和体积都保持最小，同时允许您使用许多不同的热端。每个 hotend 的设置都可以单独配置，你甚至可以一起使用[不同型号的 hotend](http://hackaday.com/2015/11/18/diamond-hotend-opens-the-color-gamut-for-3d-printing/)(可能一个型号更适合 PLA，而另一个更适合 ABS)。该设计仍处于原型阶段，需要一些改进，但这是一个非常有前途的概念证明，似乎可以很容易地在大多数 3D 打印机模型中实现。

 [https://www.youtube.com/embed/eOKCvtaMa08?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/eOKCvtaMa08?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

