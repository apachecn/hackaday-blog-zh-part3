# 微型发射器跟踪目标

> 原文：<https://hackaday.com/2017/12/23/tiny-transmitter-tracks-targets/>

这是间谍电影的主要内容。英雄——或者有时是坏人——将一个不会比苏打水大的装置贴在一辆车或一个人身上，然后追踪它到世界上的任何地方。现实世界的物理让我们很难想象这样的设备，原因有很多。微小的电源意味着微小的寿命和低功率。微小的天线和低功率可能导致短距离。然而，[汤姆的 Hackaday.io 项目可能是你能找到的最接近詹姆斯·邦德式追踪器的项目了。你可以在下面看到这个设备的视频。

这个小发射器比拇指指甲还小——不包括天线和电池——并且消耗的电流非常少(180 uA)。正如你所料，范围不是很大，但[汤姆]说，有了八木和 RTL-SDR，他可以跟踪发射机在 915 兆赫约 400 米。

如你所料，电路很简单。低频振荡器(大约半赫兹)触发带有 SAW 谐振器的 RF 振荡器。一个双极晶体管驱动一个简单的鞭状天线。原理图和更多细节在[指令栏](http://www.instructables.com/id/Tiny-UHF-Tracker-Transmitter/)中。

由于半赫兹计时，你大约每两秒钟就会听到一次蜂鸣声，这可能有利于电池寿命，足以进行跟踪。只是不要指望一个 GPS 坐标追踪器，你可以从半个地球之外的秘密巢穴接收到，你会没事的。

如果你有更多的空间和动力，你可以离[间谍的梦境追踪器](https://hackaday.com/2017/07/06/gps-tracker-gets-sms-upgrade/)更近一点，但只是一点点。如果你想用一个活动的 USB 端口来跟踪一些东西，你总是可以看到你能[塞到一个 USB 驱动器外壳](https://hackaday.com/2017/06/11/hackaday-prize-entry-usb-gsm-gps-9dof-sd-tinytracker-has-all-the-acronyms/)里多少东西。

 [https://www.youtube.com/embed/TDJljGdxk4M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/TDJljGdxk4M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

