# 最小的计算机和操作系统:一个按钮，一个 LED

> 原文：<https://hackaday.com/2016/10/08/minimal-operating-system-one-button-one-led/>

从任何意义上来说，DUO BINARY 都是一个非常非常小的计算机系统。它运行在 ATtiny84 上，它的名字中甚至有“tiny”这个字。用户界面是一个用于数据输入的按钮和一个用于反馈的 LED，这使得[这个二进制键盘](http://hackaday.com/2016/07/20/binary-keyboard-is-the-purest-form-of-input-device/)看起来过于复杂。它使用一个魔鬼般的摩尔斯电码和一个截短的 ASCII 码来输入数据，LED 同样会对你闪烁。

我们猜测[杰克·艾森曼]是世界上唯一能控制这个东西的人，你可以在下面嵌入的视频中看到他这样做。

但是仅仅因为这个系统是简约的，并不意味着它不强大。它有 128 K 的 SRAM 和 2 MB 的内存。)的“操作系统”可以利用的板载闪存。(我们无法想象用莫尔斯电码输入 2 MB 的数据，所以我们推测这就是为什么要插入闪光灯的原因。)有了这么多闪存，【Jack】实现了一个文件系统也就不足为奇了。

它运行一个难以置信的精简的字节码,自然是用一个定制的汇编程序组装起来的。还为好奇者( [zip 文件](http://ostracodfiles.com/binary/Storage.zip))或勇敢者提供了示例程序。

 [https://www.youtube.com/embed/d_TCPHprU3o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/d_TCPHprU3o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

