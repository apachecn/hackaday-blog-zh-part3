# DIY VT220 键盘

> 原文：<https://hackaday.com/2017/08/08/diy-vt220-keyboard/>

人们总是对旧电脑感兴趣，并且喜欢收集和修复它们。当[peterbjornx]得到一台 DEC VT220 视频终端时，它的状态很好——它需要一点清洁，但也需要一个键盘。[Peter]买不起键盘，但是有维修手册，所以他决定[改装一个现代键盘](https://peterbjornx.nl/vtkbd/)来配合他的新终端。(编者注:链接腐烂。试试互联网档案馆的 [Wayback 机器链接](https://web.archive.org/web/20180703165508/https://peterbjornx.nl/vtkbd/)吧。)

VT220 的原始键盘是 LK201。该键盘使用 [8-N-1](https://en.wikipedia.org/wiki/8-N-1) (八个数据位，无奇偶校验，一个停止位)通过 RS232 以 4800 波特与终端通信。这意味着在微控制器上实现这一点以便与终端进行通信非常简单。[Peter]选择了 Arduino Nano。然而，LK200 不仅仅是一个与终端通信的键盘，它还包含一个扬声器和 led，终端使用它们与用户通信。[Peter]没有把这些放入适配器单元，而是决定把它们放入键盘——几个孔和一些电线，它们就在里面了。

[Peter]的报告包括对他遇到的一些问题的描述以及键盘的图片。他把原理图放到了网上，代码也放到了 GitHub 上。如果你想知道，他用 VT220 上的 Vim 写他的文章。你也可以用一个[树莓 Pi 来帮助你的哑终端](https://hackaday.com/2016/10/19/dumb-terminals-and-raspberry-pis/)，或者仅仅是[把终端直接挂在你的 Linux 盒子上](https://hackaday.com/2016/10/31/by-the-glow-of-the-crt/)然后从那里开始。