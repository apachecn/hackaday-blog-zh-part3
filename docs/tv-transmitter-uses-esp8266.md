# ESP8266 在频道 3 上传送电视

> 原文：<https://hackaday.com/2016/01/31/tv-transmitter-uses-esp8266/>

我们在过去已经看到了很多 ESP8266 项目，但这一个绝对称得上是一个黑客。[Cnlohr]注意到，当超频时，ESP8266 可以以大约 80MHz 的速度操作 I2S 端口，并且仍然不会丢失 DMA 数据。他想出了如何[创建产生 60MHz 左右射频的位模式](https://github.com/cnlohr/channel3)。为什么会有意思呢？模拟电视可以在频道 3 上接收该频率附近的信号。

正如你在下面的视频中看到的，输出只是单色的，有点多雪。它也会在一些 WiFi 事件中丢失帧，但当你考虑到这个非常便宜的模块根本不打算做视频输出时，这都是可以原谅的。

你会在视频里看到超频的 ESP8266 还是挺有能力的。它可以绘制文本、2D 图形，甚至多种 3D 图形。哦，它同时也提供一个网页。如果你想自己尝试，只需将一根线焊接到设备的 RX 引脚上，并从 GitHub 加载代码。

这个[不是我们第一次](http://hackaday.com/2014/01/31/cnlohr-demos-his-photoetch-pcb-process/)(甚至不是第二次[)看到的【Cnlohr】。他的 YouTube 频道拥有从在 ESP8266 上使用 WebSockets 到微型《我的世界》服务器的一切。绝对值得一看。](http://hackaday.com/2013/02/18/cnlohrs-microscope-slide-linux-avr-minecraft-thing/)

 [https://www.youtube.com/embed/SSiRkpgwVKY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/SSiRkpgwVKY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[Rodrigo Pereira]、[Tobias]和[Lucas]的提示！