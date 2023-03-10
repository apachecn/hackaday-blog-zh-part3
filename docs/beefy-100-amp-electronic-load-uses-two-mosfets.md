# 结实的 100 安培电子负载使用两个 MOSFETs

> 原文：<https://hackaday.com/2017/02/28/beefy-100-amp-electronic-load-uses-two-mosfets/>

[Kerry Wong]有一些极端的 MOSFET(ixtk 90n 25 l 2)，并决定创建一个高电流电子负载。结果是一个[双通道 beast，每个通道](http://www.kerrywong.com/2017/01/15/a-400w-1kw-peak-100a-electronic-load-using-linear-mosfets/)可以处理 50 A。它们合在一起可以吸收 400 W 的功率，并且可以短时间处理 1 kW 的峰值功率。你可以在下面的视频中看到一个演示。

电子负载本质上是一个负载电阻，可以连接到电源，电阻由输入电压设置。因此，如果负载设置为 10 A，并将其连接到 12 V 电源，MOSFET 看起来应该像 1.2 欧姆的电阻。请记住，那是 120 瓦，比普通的白炽灯泡还要大。所以你需要带走一些热量。

电路非常简单。场效应晶体管接受栅极上的电压，这使它们看起来像一个随电压变化的电阻。一个非常小的源电阻产生基于电流的电压(50 A 电流仅 75 mV)。该电压馈入比较器，比较器在查看输入控制电压后产生栅极电压。进入比较器的每个毫伏通过负载转化为额外的 1.33 A。

使用小电流检测电压是一件好事，因为它将大部分电压留给了负载。然而，这意味着您必须谨慎选择运算放大器，使其具有极低的输入失调电压，因为在这一水平上，即使 1 mV 也超过 1%的误差。

一旦你可以用电压控制负载，下一步就是[对其进行编程](https://hackaday.com/2014/04/29/a-simple-programmable-electronic-load-using-the-arduino/)。顺便说一下，克里似乎对[电子负载](https://hackaday.com/2013/10/28/building-a-dc-constant-currentpower-electric-load/)情有独钟。

 [https://www.youtube.com/embed/Vr6YsT403DM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Vr6YsT403DM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

