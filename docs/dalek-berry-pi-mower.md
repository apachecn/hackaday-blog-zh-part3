# Dalek-Berry-Pi 割草机

> 原文：<https://hackaday.com/2015/11/02/dalek-berry-pi-mower/>

关于割草机和黑客。把它们变成聪明独立的机器人的愿望。可能是为天网有了自我意识或者博格人集体来把他们同化进蜂巢的那一天做准备。[Ostafichuk]希望他的能在这种情况下做好准备，所以他正在建造一台[覆盆子-Pi 动力、Dalek 服装的割草机](http://www.ostafichuk.com/raspberry-pi-projects/raspimower/),自 2014 年启动以来，这项工作仍在进行中。根据他的说法，“商用机器人割草机太贵了，也不够恐怖，没有任何乐趣，所以我想我只能自己造一些东西了……”

他的第一份报告描述了他用碎木片建造的基本骨骼结构。两个大型草坪拖拉机轮和第三个枢轴轮有助于移动。两个大轮子由齿轮电机驱动，最初用于汽车座椅高度调节。一个深循环 12V 电池，充电用的太阳能电池板会照顾电力。raspberry-pi 为 Dalek 割草机提供脑力，基于 L298N 的驱动器帮助驱动电机。这具尸体是由他四处堆放的一些废木板搭建而成的。[在等待几个部件到达的时候](http://www.ostafichuk.com/raspberry-pi-projects/raspimower/raspimower-october-progress/)——超声波传感器、加速度计、5V 电源模块——他开始油漆和装饰木制品。大量的防水涂料和胶带被用来使它不受天气影响。他最初的计划是用 python 写代码，但后来他转而用 c 语言和 [wiringPi 库](http://wiringpi.com/)一起编程。该项目的代码可以从他的 [bitbucket git 库](https://bitbucket.org/ronostafichuk/raspimower)获得。负载测试显示 L298N 驱动器不适合电机产生的高电流，因此他改用继电器来驱动它们。

在开始割草部分的工作之前，Dalek 割草机在万圣节期间得到了很好的利用，之后他将硬件放入仓库，并开始编写代码。他的目标之一是将 Raspberry-pi 摄像机用于视觉系统，并在他的院子周围设置路标。让拉斯皮卡姆工作起来比他预期的要困难。在徒劳地努力让他的 C 代码工作之后，他转向使用 C++。这一部分看起来仍然需要改进，它似乎将 Pi 扩展到了它的计算极限。最终，他删除了自己编写的所有 raspicam 功能，转而使用另一个[视频流解决方案](http://www.ostafichuk.com/rasberry-pi-fast-video-streaming-to-web/)。

 [https://www.youtube.com/embed/mobE27f4jHY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mobE27f4jHY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



一个[网络界面](http://www.ostafichuk.com/raspberry-pi-projects/raspimower/web-interface-for-raspimower/)现在允许他远程控制 Dalek-Mower 上的功能，如电机运动控制、播放音频剪辑、照明控制和其他几个未来使用的功能-割草机、巡逻、消防炮。[ostafichuk]在近一年的时间里投入了大量的工作，我们希望他能为未来我们遇到的任何科幻场景做好准备。查看下面由[ostafichuk]-junior 通过平板电脑控制的 Dalek 割草机视频。

说到这个话题，看看这个机器人割草机，它是今年唯一一个进入[hack aday 奖](http://hackaday.io/prize)半决赛的家用机器人。