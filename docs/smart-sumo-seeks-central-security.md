# 智能相扑寻求中央安全

> 原文：<https://hackaday.com/2015/10/19/smart-sumo-seeks-central-security/>

Pololu 公司的[David]设计了一个迷你相扑机器人[Zumo Red，带有一些额外的智能](https://www.pololu.com/blog/543/sumo-ring-border-angle-detection)。

相扑机器人的基本规则就像人类相扑一样——把你的对手推出拳击场。[David]的机器人很特别，因为它不仅能探测比赛边界，还能测量机器人与圆周的角度。知道了角度，[大卫]的机器人就可以转身跑向竞技场的中心，最安全的位置。一旦安全，它就可以从象征性的制高点攻击竞争对手。不幸的是，在已经很低重量级的比赛中，这个机器人是轻量级的。它未能将任何竞争对手挤出擂台，在面对面的战斗中也表现不佳。[![0J6807.550](img/5c97c9c6109c7ecdfec62d364800db5d.png)](https://hackaday.com/wp-content/uploads/2015/10/0j6807-550.png)

[David]的机器人使用三个 LED 线传感器来检测边界，这在今天的线跟踪中很常见。当机器人移动时，外部传感器会检测到边界。它继续向前行驶，直到中间的传感器被击中。它提供了计算角度所需的测量值。利落简单！知道了角度后，机器人快速移动到中心，计划下一次攻击。

[大卫的]为他的机器人大脑制作了[代码，这是一个兼容 Arduino 的 ATmega32U4，所以看看竞争对手是否会采用这个技巧将会很有趣。](https://github.com/DavidEGrayson/zumo-red/tree/lvbots_sumo_2015)

休息之后，Zumo Red 在视频中遇到了 Sumo Necko 和其他几个竞争者。

 [https://www.youtube.com/embed/o-uQjFoeFxU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/o-uQjFoeFxU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

