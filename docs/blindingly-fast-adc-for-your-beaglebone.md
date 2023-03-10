# 令人眼花缭乱的快速 ADC 为您的猎兔犬骨

> 原文：<https://hackaday.com/2016/07/31/blindingly-fast-adc-for-your-beaglebone/>

[Jason Holt]来信告知他的 pru DAQ 项目的发布。它是一个双通道 10 位 ADC cape，与 [BeagleBone 的可编程实时单元(PRUs)](https://hackaday.com/2014/06/22/an-introduction-to-the-beaglebone-pru/) 相连，每个通道每秒可穿梭多达 20 兆样本。这是很大的带宽！

诀窍是用 pru 读取 ADC，pru 本质上是电路板上内置的一点可编程逻辑。只需一点 PRU 代码，数据就能以你所希望的最快速度从 ADC 传送到 BeagleBone 的内存中。的确，对于[Jason]写的演示代码来说太快了，它甚至不能那么快地访问 RAM。相反，你会想要使用来自 [BeagleLogic 项目](https://github.com/abhishek-kakkar/BeagleLogic)的定制内核驱动程序(在之前我们已经[在这里讨论过)。](https://hackaday.com/2015/02/19/turn-your-beagleboneblack-in-to-a-14-channel-100msps-logic-analyzer/)

但即便如此，如果你不想在船上处理数据，你必须以某种方式把它拿出来。100 兆以太网每秒能给你 11.2 兆字节，一个精选的闪存驱动器每秒能节省 14-18 兆字节。但是，两个 10 位 ADC 以每秒 20 兆样本的速度全速运行，每秒产生大约 50-80 兆字节。关键是，PRUDAQ 正在产生一个*吨*的数据。

那么这个斗篷有什么用呢？它仅限于 ADC 的 2v 输入范围，需要对信号进行预处理，才能用作通用示波器。您也可以多路复用 ADC，允许 8 路输入，但当然不是同时输入。但是，例如，两个高带宽通道将成为定制 SDR 设置的绝佳后端。在一台单板计算机上获得如此大的 ADC 带宽是一个了不起的技巧，过去要花费数千美元。

我们问[杰森]他为什么要建造它，他说他不能告诉我们。这是一个谷歌的研究项目，所以让疯狂的猜想节开始吧！