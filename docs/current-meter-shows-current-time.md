# 电流表显示当前时间

> 原文：<https://hackaday.com/2016/01/05/current-meter-shows-current-time/>

这不是第一个这种类型的时钟，但是[Daniel]的基于 MSP430 的模拟仪表时钟无疑是一个“黑客”商。他承认，我们不久前推出的一款早期[伏特计时钟](http://hackaday.com/2012/08/24/volt-meter-clock-also-displays-the-temperature/)激发了他打造自己版本的灵感。

[Daniel]正在学习嵌入式系统课程，需要构建一个基于 MSP430G2553 微控制器的最终项目。这就是为什么他决定使用微控制器本身来实现实时时钟，而不是使用外部 RTC 模块。这也简化了所用的硬件——微控制器、一个晶体、三个模拟电流表和几个无源器件就是他所需要的全部。除了电流表，其他东西都来自他的零件箱。新面板放在电流表上，电路装配在一块条形板上。一块弯曲的钢板用作外壳。

有趣的部分是软件。他是用纯 C 编写的，没有借助 Energia IDE。他在他的博客文章中介绍了他的[代码](http://pastebin.com/rc3EDt9r)的所有重要部分。为定时晶体设置负载电容很重要，所以他用示波器做了一个实验，看看哪个值效果最好。TI 的[关于 MSP 430 32 kHz 晶体振荡器](http://www.ti.com/lit/an/slaa322b/slaa322b.pdf) (PDF)的应用笔记被证明是一个有用的资源。三个 PWM 输出运行三个电流表，显示小时，分钟和秒。按钮开关让他设置时钟。在下面的视频中可以看到这个时钟的简短演示。

 [https://www.youtube.com/embed/dqn5BisP4No?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/dqn5BisP4No?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

