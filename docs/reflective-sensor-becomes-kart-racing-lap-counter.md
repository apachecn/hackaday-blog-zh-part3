# 反光传感器成为卡丁车比赛圈计数器

> 原文：<https://hackaday.com/2017/07/15/reflective-sensor-becomes-kart-racing-lap-counter/>

一旦你有了一条赛道和一辆可以在上面比赛的卡丁车，还缺什么？显然，一个圈计数器可以给出你的圈速。这就是为什么[the_anykey]创造了基于 Arduino 的圈速计时器来帮助他和他的孩子节省跑步的宝贵时间，并配有热敏打印机来打印结果。

该硬件使用红外光束传感器模块(Velleman PEM10D)来检测卡丁车何时经过。该模块类似于放大的红外反射物体传感器；它在一端结合了红外发射器和接收器，并指向放置在轨道上的反射器，最远可达 10 米远。当卡丁车中断光束时，模块将事件报告给其余的硬件。仅在一侧需要电子设备就允许该单元是独立的。

这个系统的一个明显的缺点是无法区分多辆赛车，但对于单个车手的表现来说，它可以做到。这个项目的伟大之处在于，它展示了如今硬件是多么容易接近；像这样的设备可以与任何爱好者都可以使用的现成组件组装在一起，使用 Arduino 作为胶水将它粘合在一起。我们只是评论说，一块红色塑料作为红色显示屏的覆盖层(一块灰色塑料作为绿色显示屏的覆盖层)会使 LED 显示屏更容易阅读。尽管如此，这仍然是一个非常干净和有据可查的构建。在下面嵌入的视频中查看它的运行情况。

 [https://www.youtube.com/embed/bH3H8ah9JDQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/bH3H8ah9JDQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



如果可以处理多辆车的比赛计时更符合你的速度，我们之前已经看到了用于无人机比赛的 DIY 计圈器。