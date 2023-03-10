# 机械闭环步进伺服为每个人

> 原文：<https://hackaday.com/2016/06/01/mechaduino-closed-loop-stepper-servos-for-everyone/>

是水里的东西，还是最近有很多[真的很酷的伺服项目](https://hackaday.io/project/11224-mechaduino)？Mechaduino 是一个电路板，它位于常规的步进电机上，并将其转换为具有 0.1 度闭环控制的伺服系统

每当我们发布一些关于使用[廉价无刷电机进行精确控制的东西，](http://hackaday.com/2016/05/23/hackaday-prize-entry-industrial-servo-control-on-the-cheap/)有人评论说，步进电机只是一个有很多磁极的无刷电机，为什么不像一个一样控制它。这正是机械人所做的。他们还暗示用电路板上的磁性编码器做一些非常聪明的事情，这允许他们在例行校准后，获得他们承诺的精度。

这个名字听起来有点像 Arduino，因为它们与 Arduino 开发环境完全兼容。主板的大脑是兼容的 SAMD21 ARM M0+芯片。他们希望公告板尽可能容易接近。除此之外，它还允许用户对电路板使用任何想要的控制算法。大多数工业控制器仅限于 PID 控制，用于返回到最后发送的位置。开放控制允许有趣的应用，例如行为像质量弹簧阻尼系统的马达，或电子传动一个步进器的输入到另一个的输出。

该板支持许多标准通信协议，但接受常规步进输入使其更加有趣。它可以取代普通 CNC 或 3D 打印机上的电机，后者具有完全闭环控制，如休息后的视频所示。

他们打算继续做这个项目，直到它达到可以启动的水平。然而，有兴趣的读者可以浏览 GitHub 上的所有设计文件，并在今天开始使用它，而不是像一些人所做的那样含糊地承诺在发布后的某个时间发布一个开源版本。[固件](https://github.com/jcchurch13/Mechaduino-Firmware)和[硬件](https://github.com/jcchurch13/Mechaduino-Hardware)。

 [https://www.youtube.com/embed/T1HIWAiMrfY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/T1HIWAiMrfY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

