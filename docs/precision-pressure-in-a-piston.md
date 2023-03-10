# 活塞中的精确压力

> 原文：<https://hackaday.com/2017/05/09/precision-pressure-in-a-piston/>

[Scott]正在为他的水族馆建造一个 DIY 酵母反应器。什么是酵母反应器？[Scott]想把二氧化碳泵入他的水族箱，这样他的水生植物就能长得更多。他将一加仑含糖的发酵水注入一个装有植物和鱼的水槽中。换句话说，[斯科特]正在做这整个事情完全落后，并利用酵母代谢的错误废物。

然而，在向他的水族馆泵入二氧化碳的过程中，[斯科特]创造了一个非常高精度的压力传感器。它基于具有 MS5611 气压传感器的分线板。它有一个 24 位 ADC，可以转换成每平方英寸万分之一磅的压力。

为了将这种压力传感器集成到水族馆/水族馆的设置中，[Scott]用注射器制作了一个压力计。注射器的柱塞端包裹在环氧树脂中，尖端仍然能够接受针头，[Scott]能够轻松地将这个传感器插入他的酵母反应器。来自传感器的数据可通过 I2C 访问，带有 ATmega328 和字符 LCD 的简单电路显示注射器中的当前压力。

我们以前见过这些高分辨率压力传感器在无人机和火箭中用作高度计，但从未用作压力计。然而，这是一种测量真空和一个大气压之间压力的廉价而新颖的解决方案。

 [https://www.youtube.com/embed/T3ma1n_jhbQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/T3ma1n_jhbQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

