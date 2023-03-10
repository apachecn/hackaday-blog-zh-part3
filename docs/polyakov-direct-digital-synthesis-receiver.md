# 波利亚科夫直接数字合成接收机

> 原文：<https://hackaday.com/2015/11/15/polyakov-direct-digital-synthesis-receiver/>

直接变频接收机在业余无线电爱好者和其他无线电制造商中很受欢迎。假设你想听一个 7.1 MHz 的信号。对于直接变频接收机，您需要将本机振荡器调谐至 7.1 MHz，并将其与输入信号混频。所得到的输入频率的和与差将包括期望频率上的 AM 信号的音频。

[kk9jef]决定[为 40 米波段](https://kk9jef.wordpress.com/2015/11/09/40m-direction-conversion-receiver-in-the-polyakov-style/)(约 7 MHz)建造一个这样的接收器。他从一个早期的设计开始，用他以前建造的 Si5351 DDS VFO 取代了它的模拟 VFO(并使用无处不在的 Arduino)。一个有趣的变化是:最初的设计使用波利亚科夫或俄罗斯的检波器，需要一个“半频”本地振荡器。也就是说，要调到 7.0 MHz，你实际上调到了 3.5 MHz。这有时被称为次谐波混频器。优点是较低频率的振荡器更容易稳定。最初接收器的设计者【ke3ij】，[在他的测试](http://www.ke3ij.com/DC-80.htm)中有一篇有趣的文章来揭示为什么这个方案有效。

最初的设计是针对 3.5 MHz 频段(并使用 1.25 MHz 本地振荡器)。[kk9jef]重新设计了输入滤波器，以适应新的工作频段。驱动本地振荡器的 Arduino 软件也读取编码器并驱动 LCD。让它读取实际工作频率是一件简单的事情。

当然，以较低的频率运行 Si5351 可能没有太大的优势。它应该在任何能振荡的地方都能正常工作。在之前，我们已经介绍过使用这种芯片的可变频率振荡器[，如果你想知道的话，我们自己的【Bil Herd】](http://hackaday.com/2015/10/13/triple-frequency-vfo-on-a-bamboo-breadboard/)[在下面的视频中解释了这种芯片如何在内部运行](http://hackaday.com/2014/11/24/direct-digital-synthesis-dds-explained-by-bil-herd/)。

 [https://www.youtube.com/embed/MKiP-4o3cFI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MKiP-4o3cFI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

