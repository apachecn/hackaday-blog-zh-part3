# 睡觉时记录你的体重

> 原文：<https://hackaday.com/2017/12/12/keep-track-of-your-weight-while-sleeping/>

一般人看一张床，都会想到睡觉。因为这就是床的作用。你用柔软温暖的布和蓬松的枕头盖住它们，然后睡在上面。[彼得]不是一般人。他是个创造者。当他看着一张床时，他会考虑让它有能力追踪自己的体重。

宜家床的每只脚下有四个中国制造的 TS-606 称重传感器，配有定制的铝制外壳。每一路信号都进入 HX711 模数转换器，后者提供 24 位分辨率。这些馈入 Arduino Nano，Arduino Nano 又通过 USB 到 UART 桥连接到 Raspberry Pi。连接到 Pi 允许[Peter]将数据上传到他的家庭网络，在那里他将数据绘制到 [gnuplot](http://www.gnuplot.info/) 。

这款智能床不仅能追踪[彼得]的体重。它还可以跟踪房子里其他人的体重，包括他的宠物。请务必查看他的 [GitHub](https://github.com/ptwz/bedscale) 以获得完整的源代码。