# 一次修复一个芯片组的 Linux 音频

> 原文：<https://hackaday.com/2017/11/25/fixing-linux-audio-one-chipset-at-a-time/>

对于外行来说，Linux 音频可能会令人困惑。随着时间的推移，作为一个已经进化并产生了至少两个独立分支的系统，它往往会产生令用户惊讶或恼怒的结果。另一方面，它是开源软件，因此，如果你知道你在做什么，它是可以修复的。

Reddit【rener 2】感到恼火的是，在他的笔记本电脑上听音乐，在 Linux 下比在 Windows 下体验差得多。运行 Windows 时，耳机插孔的输出覆盖了整个频谱，而他的 Linux 设置切断了低端，导致声音微弱。罪魁祸首是声卡:它有两条不同的输出路径，分别用于内部扬声器和耳机插孔。内部扬声器的信号通过高通滤波器传送，以避免无法再现低频的尴尬。

当耳机插入时，声卡驱动程序应该使声卡绕过滤波器，并提供全频谱。Windows 驱动程序的作者知道这一点，并且已经解决了这个问题。在他的[视频](https://www.youtube.com/watch?time_continue=971&v=a1YkPtfC4LI) [rener2]向我们展示了修补 ALSA 驱动程序的过程，同时参考了他认为与他的 Realtek ALC288“足够相似”的声卡的文档。

 [https://www.youtube.com/embed/a1YkPtfC4LI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/a1YkPtfC4LI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



一旦你弄清楚了你的音频设置，你应该考虑试试用八度音程处理[信号。或者你可以完全抛弃支持不佳的硬件，在你的树莓派上贴一个](https://hackaday.com/2016/06/30/tutorial-on-signal-processing-in-linux-with-octave/)[像样的声卡](https://hackaday.com/2017/03/16/pisound-the-audio-card-for-the-raspberry-pi/)。