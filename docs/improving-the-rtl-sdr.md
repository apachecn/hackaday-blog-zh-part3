# 改进 RTL-SDR

> 原文：<https://hackaday.com/2016/03/28/improving-the-rtl-sdr/>

RTL-SDR 加密狗是无线电黑客的真正主力。然而，板载的 28.8 MHz 振荡器并不像你希望的那样稳定。这对于很多应用程序来说都很好，考虑到价格，你不应该抱怨。然而，在某些情况下，您需要更稳定的参考频率。

[Craig]想要一个稳定的解决方案，立即想到了 TCXO(温度补偿“Xtal”振荡器)。问题是，在 28.8 MHz 下找到这些很难，即使能找到，也相对昂贵。他决定[用一种更容易找到的 19.2 MHz 晶体制作一个替代振荡器](http://www.analogzoo.com/2016/03/building-a-better-rtl-sdr-tcxo/)。

如何将 19.2 MHz 信号转换为 28.8 MHz？首先，你需要一个触发器将输出频率除以二。这就产生了 9.6 MHz 方波。这似乎并没有好到哪里去，直到你想到是什么产生了方波。[傅立叶级数](http://hackaday.com/2015/09/17/visualizing-the-fourier-transform/)告诉你方波是正弦波的无限和。一个正弦波处于基频，然后其他正弦波处于每个奇次谐波(即 3X、5X、7X 等)。而 3 * 9.6 就是 28.8，正是你需要的！

[Craig]所要做的就是对触发器的输出进行滤波，以产生精确的 28.8 MHz 信号。他提供了所有必要的数据来复制他的设计，你可以在下面的视频中看到他的测试。

从 TXCO 的下一步是一个烤箱(OCXO)。我们已经看到一些自制 OCXOs 应该可以用同样的技巧工作。

 [https://www.youtube.com/embed/ZdlSHtGH8EI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZdlSHtGH8EI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

