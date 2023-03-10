# Arduino 做硬科学

> 原文：<https://hackaday.com/2017/06/28/arduino-does-hard-science/>

我们不知道为什么[stoppi71]需要做伽马能谱。我们只知道[他做了一个](http://www.instructables.com/id/Multi-Channel-Analyzer-for-Gamma-Spectroscopy-With/)，包括高压电源、光电倍增管，还有——还有——一个 Arduino。你还需要一个闪烁晶体来将伽马射线转换成可见光，以便电子管接收。

他开始使用名为[的开源多通道分析仪(MCA)进行测试。它通过声卡连接，在个人电脑上运行。然而，他想自己滚动，用一些简单的电路和一个 Arduino 来实现。](http://www.theremino.com/en/blog/gamma-spectrometry)

该管检测晶体中非常微弱的光，因此它们需要在不透光的外壳中。Arduino 需要一点帮助来以简单电路的形式读取来自电子管的脉冲。该电路充当峰值检测器，峰值仅持续大约 20 微秒。帖子没有峰值检测器的原理图，但下面的视频有。

如果你想了解分光计项目，请查看 [Hacklet 122](https://hackaday.com/2016/08/27/hacklet-122-spectrometers/) 。不可否认，我们看到的大部分都是依靠[可见光](https://hackaday.com/2016/08/01/hackaday-prize-entry-a-visible-spectrophotometer/)。

 [https://www.youtube.com/embed/6k9pkbhxa00?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6k9pkbhxa00?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

