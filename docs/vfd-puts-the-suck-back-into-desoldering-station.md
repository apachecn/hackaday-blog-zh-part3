# VFD 将吸管放回脱焊站

> 原文：<https://hackaday.com/2017/12/22/vfd-puts-the-suck-back-into-desoldering-station/>

如果你从事从旧设备中回收零部件的业务，专用的拆焊站是一个非常好的工具。在单个工具中加热和抽吸远比用弹簧加载的焊料吸盘或编织物更方便，但前提是脱焊工具中的抽吸有一点吸引力。因此，如果你的焊钳上的吸力开始吮吸，[这个简单的 VFD](https://www.youtube.com/watch?v=mEiUt56elAw) 可以帮助恢复性能。

对 Carlson 先生]来说幸运的是，他的 Hakko 470 脱焊站配备了交流感应电机，因此它是变频驱动的完美候选，以提高性能。他决定建造一个简单的 VFD，将电源频率从 60 赫兹提高到大约 90 赫兹，从而将电机速度提升 50%。VFD 只是一个 TL494 PWM 芯片，通过 MOSFET 控制电源变压器的初级线圈。占空比和频率由修整器设定，整个装置装在一个旧底盘上，通过真空管时代的过时插座和插头连接到 Hakko 上。不过，这是一个不错的想法，因为 Hakko 可以通过一个简单的桥接插头返回到库存操作，下面的视频显示了插上和不插上 VFD 时电机速度的显著差异。

我们曾惊叹于[卡尔森先生]的[仪器挤满了实验室](https://hackaday.com/2017/09/06/ask-hackaday-how-small-is-your-shop/)，并观看了[他的内幕之旅的老式无线电发射机](https://hackaday.com/2017/04/05/retrotechtacular-a-walk-in-broadcast-transmitter/)。希望我们能很快看到更多他的焊锡膏。

 [https://www.youtube.com/embed/mEiUt56elAw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mEiUt56elAw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

