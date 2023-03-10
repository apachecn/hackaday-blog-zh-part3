# ESP32 成为世界上最差的电台

> 原文：<https://hackaday.com/2018/01/28/esp32-makes-for-worlds-worst-radio-station/>

我们可以为[bitluni]说一件事:他的项目的材料清单，像[这个 ESP32 AM 无线电发射机](http://bitluni.net/am-radio-transmitter/)，总是偏低。这是因为他利用软件来完成传统上由硬件完成的工作，并且总是有启发性的结果。

在这种情况下，手头的工作是在广播 AM 波段创建一个 RF 振荡器，并在其上调制一些音频。根据他之前使用 ESP32 在示波器上观看视频的经验，【bitluni】知道微控制器的 DAC 能够产生 800 kHz 的信号，他设法用一些巧妙的代码产生了一个或多或少的正弦波载波。他的草图从一个头文件中提取数据，将其调制到载波上，并使用一根短电线作为天线通过以太网发送出去。范围是非常有限的，但就其本身而言，它完成了工作并展示了基础。另外，[bitluni]包含了一点 JavaScript，可以将一个音频文件转换成一个头文件，随时可以通过广播发送出去，满足您的所有需求。

如果你正在为你的低功率发射机寻找一个更大的范围，并且你是一个有执照的业余操作者，你可能想探索一下[QRP 无线电](http://hackaday.com/2016/03/08/how-low-can-you-go-the-world-of-qrp-operation/)的世界。

 [https://www.youtube.com/embed/lRXHd3HNzEo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lRXHd3HNzEo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

