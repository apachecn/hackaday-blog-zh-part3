# 调幅超声波发射器和接收器

> 原文：<https://hackaday.com/2018/03/06/am-ultrasonic-transmitter-and-receiver/>

超声波传感器通常用于距离测量，在 DIY 世界中，通常作为机器人探测障碍物的一种方式。但是对于一个周末项目，[Vinod。S]从测距仪模块中取出超声波发射器和接收器，[使用振幅调制将音乐从他的笔记本电脑超声发送到扬声器](http://blog.vinu.co.in/2018/03/ultrasonic-audio-transmitter-and.html)，本质上是发送和接收无声的调制声波。

[![The transmitter and receiver](img/04f77b6fc5de58afa6e1d8582c332a27.png)](https://hackaday.com/wp-content/uploads/2018/03/am_ultrasonic_transmitter_and_receiver.jpg)

The transmitter and receiver

对于发射器，他将 Arduino Pro Micro 变成了可以插入笔记本电脑的 USB 声卡。它输出音频信号和 40 kHz 载波信号，使用 Arduino 的定时器 1 实现。这些信号进入他设计的电路板，该电路板使用单个晶体管用音频信号调制载波，然后将结果发送到超声波发射器。

他小心地传输清晰的信号，方法是在示波器上观察调制波，寻找过调制和削波，同时调整位于晶体管、来自 Arduino 的 5 V 电压和发射器之间的电阻值。

他同样小心翼翼地设计了接收器端。从概念上讲，这里的电路很简单，由超声波接收器、一个用于调制波的晶体管放大器、一个用于解调的二极管、另一个晶体管放大器和一个 D 类放大器组成，最后连接到扬声器。

由于低 40 千赫载波频率，声音缺乏较高的音频频率。但由于他努力调整电路，声音变得响亮而清晰。请查看下面的视频以获得概述，并亲自聆听声音。警告:在出现评论风暴之前，是的，视频是不稳定的，但我们认为黑客的质量足以弥补这一点。

你还能用超声波传感器做什么？你可以把它们连接到树莓派上，做成一个钢琴接口。或者你可以使用一个更大的换能器[来制造一个便宜的超声波烙铁](https://hackaday.com/2016/05/09/an-affordable-ultrasonic-soldering-iron/)。

 [https://www.youtube.com/embed/M9EXBVwhm8A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/M9EXBVwhm8A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

