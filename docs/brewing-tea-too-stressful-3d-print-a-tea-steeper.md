# 泡茶压力太大？3D 打印一个茶叶浸泡器

> 原文：<https://hackaday.com/2015/09/13/brewing-tea-too-stressful-3d-print-a-tea-steeper/>

当你想喝一杯热茶放松一下时，你最不需要的就是把茶包泡进和泡出热水的压力，对吗？[Andylear]对此感到厌倦，他有一台 3D 打印机，所以他着手解决这个问题。

该解决方案使用一个标准的迷你伺服系统和 VarSpeedServo Arduino 库。这个库使用中断来控制多达 8 个伺服的速度和位置。所有的伺服系统可以同时运行，你可以控制伺服系统的位置和运动的速度。命令可以是异步的，或者你可以等待它们完成，你甚至可以向每个伺服系统发送命令序列。

令我们惊讶的是，虽然我们确实看到了一些(比如[这个定时器](http://hackaday.com/2012/02/03/kitchen-timer-makes-mario-your-sous-chef/)或者[为浓缩咖啡调整 PID](http://hackaday.com/2011/11/27/kitchen-hacks-improving-an-espresso-machine/)),但是没有更多的厨房黑客。我们之前甚至见过[的另一个茶叶自动化项目](http://hackaday.com/2015/01/28/automated-tea-maker/)。虽然对一些人来说这可能看起来很无聊，但这种重复运动机器在许多工业过程中是一种主食，如果它将 PC 板浸泡在蚀刻剂中或将电路板浸泡在清洗槽中，它可能会得到更多的尊重。

如果你想看 VarSpeedServo 的更费力的例子，看看下面的视频。

 [https://www.youtube.com/embed/t4KRksxjP6k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/t4KRksxjP6k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

