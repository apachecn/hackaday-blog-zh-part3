# 有趣的 USB 固件故障

> 原文：<https://hackaday.com/2016/10/04/glitching-usb-firmware-for-fun/>

[Micah Elizabeth Scott]，又名[scanlime]，一直在玩 USB 绘图板，并获得了她想要的固件-逆向工程，看看发生了什么，谁知道还有什么。Wacom 没有将这些设备设计成用户可更新的，所以没有 rom 的副本在网上流动，而且平板电脑的微控制器似乎被锁定以启动。

随着简单的途径出现死胡同，这意味着建立一些定制的硬件来完成它，并制作一个非常详细的视频记录项目(嵌入下面)。如果你对芯片电源故障攻击感兴趣，如果你没有注意力持续时间短的问题，请观看它，这是一个非凡的介绍。

剧透:ROM 转储出现在 USB 设备枚举器字符串中。使用[芯片密语器](http://hackaday.com/2015/02/27/chipwhisperer-hits-kickstarter/)(2014 年 Hackaday 奖第二名！)和她自己设计的“[face whisper](https://github.com/scanlime/facewhisperer)”附加板，[迈卡]可以在平板电脑向电脑识别自己时发送电源故障。它没有在几个设备描述符字节后停止，而是继续前进。去吧。事实上，在许多暴力尝试之一中，它两次转储其 ROM，从而很容易找到代码流的开头和结尾。

接下来是反汇编和逆向软件，这是一个不小的壮举。我们迫不及待地想看看[迈卡]会提出什么。

感谢[Ben]和[Tim]几乎同时给出的提示。

 [https://www.youtube.com/embed/TeCQatNcF20?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/TeCQatNcF20?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

