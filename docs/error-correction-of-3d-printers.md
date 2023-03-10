# 3D 打印机的误差校正

> 原文：<https://hackaday.com/2016/04/07/error-correction-of-3d-printers/>

从最早的 RepRaps 到 Makerbot 生产线上最新的打印机，几乎每台消费级 3D 打印机都有一个重大缺点:无法从错过的步骤、打滑的皮带或过热的步进驱动器中恢复。虽然这些是相当罕见的问题，但它确实会发生，而且纯粹是 3D 打印机固件中使用的~~闭环~~开环控制系统的产物。

[克里斯·巴尔]想出了一个相当聪明的办法来解决这个问题。他设计了一个系统[，可以检测和纠正 3D 打印机的机械问题](http://chrisbarrbuilds.com/2016/04/3d-printer-error-detection/)。从技术上讲，这不是一个闭环控制系统，但它允许他获得构建板上喷嘴的绝对位置，检测错误状态，并可以自动计算每毫米的电机步数。它也比我们过去见过的[其他闭环控制系统](http://hackaday.com/2015/01/20/closed-loop-control-for-3d-printers/)简单得多，只需要几个小零件连接到轴和打印机控制器板上。

[Chris]“系统使用一个磁性编码条，一个芯片和一点点支持电路。它实际上与桌面喷墨打印机上的移动轴没有太大区别。不过，这不是闭环。固件黑客只是一个“基本的错误纠正”，将喷嘴移回到它应该在的地方。虽然这有点像组装，但比重构整个打印机固件要简单得多。

在下面的视频中，[Chris]展示了他的解决方案，即通过在打印过程中晃动他的轴来纠正打印机的错误。喷嘴奇迹般地回到了它应该在的地方，产生了一个可用的零件。

 [https://www.youtube.com/embed/mVs932wOgJY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mVs932wOgJY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

