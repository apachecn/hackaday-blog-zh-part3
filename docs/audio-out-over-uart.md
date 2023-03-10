# UART 上的音频输出

> 原文：<https://hackaday.com/2016/04/11/audio-out-over-uart/>

普通标准的串行端口永远不会消亡是有原因的。它是如此的强大和简单。当你需要一个绝对可以用最少的软件和硬件工作的控制台时，UART 是个不错的选择。正因为如此，UART 黑客比比皆是。这对我们来说是一个新的挑战，对我们的读者来说也是一个挑战。

[Tiziano Bacocco]决定[使用 UART 信号作为一种 PWM 来创建音频](http://linuxehacking.ovh/2016/03/30/ft232rl-usb-serial-sound-card-hack/)。没错，他正在将串行 TX 线直接插入扬声器。这为您提供了八种可能的 PWM 输出电压电平。诀窍是使用一些 Python 代码(使用令人敬畏的 [pyserial](https://pypi.python.org/pypi/pyserial) 模块)来下量化音频数据，以适应这八个可能的值，然后以正确的采样率推出它们。`ffmpeg`用于预处理文件。

虽然对马里奥来说听起来足够好(见下面的视频)，但三位音频对演讲或复杂的音乐来说听起来不太好。所以这就是我们的挑战:用 DPCM 再做一次。不是发送电压电平，而是通过串行线发送所需的电压*变化*。由于声音和音乐声波是连续的(从数学意义上来说)，即使只有几个巧妙选择的输出，这也能很好地工作。

这里有一个让你入门的教程。您需要对输出进行积分(考虑 RC 滤波器)，并且希望将其放入放大器，但我们打赌它可以输出不错的语音。我们打赌这可以用几行 Python 代码来完成。请在下面的评论中发表你的解决方案。

尽管如此，[蒂齐亚诺]的黑客是了不起的。我们喜欢将串口直接插入放大器的简单性！那是硬核。

 [https://www.youtube.com/embed/1N7P7wvlnts?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1N7P7wvlnts?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

