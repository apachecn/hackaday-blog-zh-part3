# 带双控制器的云台

> 原文：<https://hackaday.com/2016/08/30/pan-and-tilt-with-dual-controllers/>

不久前，面对一个控制器项目，您可能会购买一些功能正好合适的东西，并试图将成本降至最低。这些天，如果你只是做一次性的，它可能会很容易扔在它的商品硬件。毕竟，一个树莓派的价格比一顿美餐还低，而且比不久前的一台完整的个人电脑还要强大。

当[Joe Coburn]想做一个云台摄像头时，他没有试图找到一个最小的配置。他刚刚扔了一个树莓 Pi 来连接互联网，还扔了一个 Arduino 来控制两个 RC 伺服电机。一条拉链带把伺服系统连在一起，还有潜在的网络摄像头。

你可以在下面的视频中看到结果。用 Pi 设置相机，向 Arduino 发送一些命令并连接到互联网是一件很简单的事情。

Arduino 的串行协议很简单:Pi 以 9600 波特发送一个数字位置，后跟一个 P(代表平移)或 T(代表倾斜)。web 服务器和一些 Python 处理互联网和人类的接口。

我们当然看到了我们在类似项目中的份额。他们中的一些已经比 T2 大了一点。

 [https://www.youtube.com/embed/1KjYMPFSKLo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1KjYMPFSKLo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

