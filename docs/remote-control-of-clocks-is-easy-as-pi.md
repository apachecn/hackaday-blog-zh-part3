# 远程控制时钟非常容易

> 原文：<https://hackaday.com/2018/04/22/remote-control-of-clocks-is-easy-as-pi/>

[Fatjedi007]最近获得了三个可编程拳击健身房类型的时钟，以帮助他的发育障碍客户管理他们的时间。该计划是让不同长度的计时器在一天中的预设时间启动，大型显示器提供任何地方的视图。不幸的是，这些时钟远不像他需要的那样可编程。

因为他已经花了足够多的钱， [[Fatjedi007]转向树莓派的力量来设计一个负担得起的解决方案](https://www.reddit.com/r/raspberry_pi/comments/8de8lg/interesting_project_i_did_at_work_with_3_pi_zero/)。每个时钟都有一个 Pi Zero W 和一个简单的 IR 发射/接收电路，该电路使用 [LIRC](http://www.lirc.org/) 进行操作。这些钟配有遥控器，所以只需要重新编程就可以了。在 LIRC，他用 SEND_ONCE 编写了一些脚本，并用 cron 作业调度计时器。不需要从梯子上下来——他可以在 VNC 上空的椅子上对它们进行编程。

不过，他确实有一个问题，那就是让零通过静态 IP 将自己设置在 NTP 上。有什么建议吗？把它们放在评论里，帮绝地一把。

LIRC 对于你想要遥控的任何东西都非常方便，比如立体声系统。