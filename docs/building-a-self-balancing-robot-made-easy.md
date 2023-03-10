# 制造自动平衡机器人变得容易

> 原文：<https://hackaday.com/2017/06/03/building-a-self-balancing-robot-made-easy/>

[Joop Brokking]不仅制造了一个容易制造平衡机器人的[,而且他还为任何想制造平衡机器人的人制作了一套极好的计划和软件。自我平衡器是你的机器人建造生涯中的一个里程碑。它们站在两个轮子上，使用 PID 控制环路来驱动两个电机，使用来自某种类型的惯性测量单元(IMU)的数据。这听起来很简单，但当从头开始时，有很多选择要做，也有很多陷阱要落入。[Joop 的]视频解释了基本原则，并涵盖了他以自己的方式做事的原因——所有你在构建自己的方式时会寻找的建议。](http://www.brokking.net/yabr_main.html)

他选择了步进电机，而不是便宜的 DC 电机，因为这样可以提高精度，避免电池电压下降时出现问题。他的软件包括一个获取 IMU 校准值的程序。他还展示了如何设置步进控制器的驱动电流。他很清楚地做到了这一切，步伐既不太快，也不太慢。他的视频绝对值得一看。

Hackaday 上有许多不同风格的平衡机器人。[Joop]的使用 Arduinos 和步进器，但是[Renee]的 [EddiePlus 使用 Intel Edison 和 Pololu DC 汽车](http://hackaday.com/2015/02/24/eddieplus-the-edison-based-balancing-robot/)。或者为什么不试试[在球上平衡而不是在轮子上平衡](http://hackaday.com/2013/10/24/building-a-ball-balancing-robot/)？为了解决 DC 汽车公司平衡机器人的问题，看看这个[基于 ATmega32U4 的开源控制器](http://hackaday.com/2017/05/18/balancing-robot-needs-innovative-controller-and-motor/)。

 [https://www.youtube.com/embed/6WWqo-Yr8lA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6WWqo-Yr8lA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

