# 用 2 轴天线定位器跟踪卫星

> 原文：<https://hackaday.com/2016/01/20/track-satellites-with-a-2-axis-antenna-positioner/>

业余无线电操作员是好奇的野兽。他们会竭尽全力进行关键的接触，确保他们的定向天线指向正确的方向是穿透的一个重要部分。当然也有商业天线旋转器，但火腿也喜欢建立自己的齿轮，像这个[树莓 Pi 控制的 2 轴旋转器](https://jkry.org/ouluhack/PiRotator)。

[wilho]的主要动机似乎是商业 2 轴旋转器的可悲的艺术状态，这似乎在 90 年代坚定地陷入困境。避开 DC 有刷电机上的模拟 pot 传感器，这种传感器似乎主导了 COTS 市场，[wilho]为移动齿轮配备了步进器和坚固的变速箱。轴上的反馈来自 10 位绝对编码器，MPU9250 9 轴 IMU 确保他确切知道天线相对于罗盘航向和仰角的指向。安装在桅杆上的 Rasp Pi 控制一切，并通过 REST API 与定制软件对话，该软件可以将天线返回到定制设置点或跟踪月球、卫星或国际空间站。这是一套令人印象深刻的装备，肯定会让你的业主协会抓狂。

对于另一个 2 轴天线定位器，请查看 [2015 年 Hackaday 奖决赛选手 SATNOGS](http://hackaday.com/2014/11/07/hackaday-prize-finalist-a-network-of-satellite-ground-stations/) 。

 [https://www.youtube.com/embed/0F_P8_iJNqI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/0F_P8_iJNqI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

