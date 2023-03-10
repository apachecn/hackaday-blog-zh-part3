# Minimin 的目标是成为最简单的特雷门琴

> 原文：<https://hackaday.com/2016/04/26/the-minimin-aims-to-be-the-simplest-theremin/>

Hackaday.io 用户[eagleisinsight]是一名高中黑客，他成为特雷门琴大师的梦想因商业乐器的高昂价格而受挫。他的回答是[Minimin，这是一个使用 555 和 ATMega328](https://hackaday.io/project/10882-minimin-mk1) 的平价特雷门设计。

555 被配置为一个非稳态振荡器，工作频率约为 5MHz，其定时电容上连接有一个环形天线。如你所料，音乐家的手对天线的寄生电容会改变振荡频率。在经典的特雷门琴中，来自 555 的信号将与固定的 5MHz 振荡器的输出混合，声音将由两个振荡器之间的差异产生，但在[eagleisinsight]的设计中，555 为 ATMega328 的计时器计时。因此，处理器可以读取振荡器频率，并使用该值来控制波形发生器。

这个特雷门琴缺少了什么:音量的第二根天线。目前，电位计可以完成这项工作，但[eagleisinsight]正在研究 MkII 设备来纠正这一遗漏，并计划用 XMega 处理器取代 ATMega，XMega 处理器的 DAC 可以产生正弦波输出，其 USB 端口可以用于启用 Minimin 作为 MIDI 控制器。

如你所料，这些年来，我们已经在 Hackaday 上讨论过无数次了。你可以[浏览它们所有的](http://hackaday.com/tag/theremin/)，但是我们想把你的注意力吸引到一个典型的[试验板乐器上，它使用一个汽水罐天线](http://hackaday.com/2014/06/01/soda-can-theremin-made-in-minutes/)，人们使用[Theremin 作为*吉他英雄*控制器](http://hackaday.com/2010/07/13/shred-air-with-theremin-hero/)，以及 Léon Theremin 的 [terpistone，一个全身乐器](http://hackaday.com/2016/01/14/retrotechtacular-the-theremin-terpsitone/)。