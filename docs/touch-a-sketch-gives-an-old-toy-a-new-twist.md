# 触摸素描给旧玩具一个新的转折

> 原文：<https://hackaday.com/2018/01/04/touch-a-sketch-gives-an-old-toy-a-new-twist/>

在经历了近 60 年的时间和大量的楼梯和广场之后，现在终于有了一种更简单的方法来绘制草图。在嵌入式微控制器课程的最终项目中，【Serena、Francis 和 Alejandro】实现了[一种电机驱动的解决方案，从触摸屏](http://people.ece.cornell.edu/land/courses/ece4760/FinalProjects/f2017/fy57_ald79_sk2282/fy57_ald79_sk2282/fy57_ald79_sk2282/index.html#intro)获取输入。

用手写笔而不是操纵杆来绘制曲线是轻而易举的事情，但它仍然是一个二维绘图仪，必须如此对待。触摸素描系统依赖于玩具的手写笔从左下角开始，因此所有杰作必须从旋钮和触摸屏上的(0，0)开始。

这个项目的 BOM 是最小的。PIC32 从触摸屏收集输入坐标，并将它们发送到一对连接到玩具旋钮的步进电机。每个电机都由达林顿阵列驱动，很快就需要一个自制的散热器，所以甚至有一个黑客。该团队无法找到可以处理电机和旋钮轴尺寸差异的耦合器，所以他们最终将电机安装在一个小胶合板桌上，并用 Velcro 将它们连接到库存旋钮上。这样做效果更好，因为蚀刻草图屏幕仍然需要用传统的方式重新设置。

他们还考虑使用[皮带来驱动旋钮，就像我们几年前看到的这个时钟](https://hackaday.com/2014/03/28/an-etch-a-sketch-to-fetch-the-time/)，但他们想避免打滑。休息之后，再倒一杯你阿姨的高辛烷值蛋奶酒，看着 Touch-A-Sketch 画出一些喜庆的东西。

 [https://www.youtube.com/embed/NBX28erLgYY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=11&wmode=transparent](https://www.youtube.com/embed/NBX28erLgYY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=11&wmode=transparent)

