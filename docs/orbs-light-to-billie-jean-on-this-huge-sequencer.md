# 在这个巨大的音序器上，宝珠照亮了比莉·珍

> 原文：<https://hackaday.com/2016/07/12/orbs-light-to-billie-jean-on-this-huge-sequencer/>

音序器让你只需将音符画在 2D 网格上就能创作出旋律，几乎可以将任何对音高和节奏感觉一般的人变成电子音乐制作人。大规模网格 MIDI 音序器 GRIDI 让音乐制作变得更加容易。

GRIDI 不用按钮，而是用球来设定音符。一旦它们被放在大板上的一个凹痕中，下次光标经过时，它们就会演奏一个音符。16 x 16 *球栅阵列*中的 256 个 RGB LEDs 根据分配给它们的乐器以某种颜色照亮球:鼓声为蓝色，低音为橙色，旋律为紫色。

 [![gridi_milling](img/cc3fa51990b00a06f75936c1fc0baaeb.png "gridi_milling")](https://hackaday.com/2016/07/12/orbs-light-to-billie-jean-on-this-huge-sequencer/gridi_milling/)  [![gridi_assembly](img/e7deac0296cca70b8ee9ddd5a850ac28.png "gridi_assembly")](https://hackaday.com/2016/07/12/orbs-light-to-billie-jean-on-this-huge-sequencer/gridi_assembly/)  [![gridi_under_the_hood](img/4829047227b1e6b3ed53b99a7cae062b.png "gridi_under_the_hood")](https://hackaday.com/2016/07/12/orbs-light-to-billie-jean-on-this-huge-sequencer/gridi_under_the_hood/) 

在 GRIDI 的 2.80 x 1.65 米(9.2 x 4.5 英尺)的 CNC 加工、打磨和彩色涂层表面下，Arduino Uno 控制所有 WS2812 LEDs 并回读用于检测球的开关。运行 Max/MSP 的主机合成系综。结果就是你将在下面的视频中看到的令人印象深刻的互动音乐艺术装置。在最初的音乐视频中，*比莉·珍*照亮的人行道给人留下了如此深刻的印象[，还有什么比这首曲子更好的呢？](https://youtu.be/Zi_XLOBDo_Y?t=20s)

 [https://www.youtube.com/embed/1K9FOuq-D9g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1K9FOuq-D9g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

