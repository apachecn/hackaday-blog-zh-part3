# 比特敲打高通充电控制器

> 原文：<https://hackaday.com/2016/12/13/bitbanging-qualcomm-charge-controllers/>

随着越来越多的制造商转向 USB-C，似乎可信的 USB 端口变得越来越根深蒂固。这也不是一件坏事。拥有这样一个通用标准对于简单性和互连性来说是非常好的。然而，如果你现在已经完全过时的一年前的手机仍然坚持使用 USB 2.0 端口，你仍然有一些希望至少可以快速充电。[hugatry]能够操纵高通的快速充电协议，使其能够与任何设备一起工作。

正在讨论的协议是*假定*只在支持的设备上工作。即任何带有高通骁龙或其他类似产品的东西。[hugatry]有一个高通快速充电功能的 USB 端口，但没有支持的设备。然而，经过一番调查后，他发现，破解协议，从高通设备中获取基本上任何数量的能量都是极其容易的。他甚至不需要微控制器来进行握手，只需要无源元件。

有点令人惊讶的是，在时代的今天[绕过一个专有标准是如此简单(他确实注意到，虽然这对他有用，但你的里程数可能会有所不同)，但我们仍然很高兴看到它。[hugatry]的过程绝对值得一试，他的视频也一样，你可以在休息后找到。](http://hackaday.com/2015/12/15/philips-says-no-internet-of-things-for-you/)

 [https://www.youtube.com/embed/UYRZ0t5eyjE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/UYRZ0t5eyjE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

