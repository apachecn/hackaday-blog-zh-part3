# 未来人造人的马达嘴

> 原文：<https://hackaday.com/2017/02/08/motormouth-for-future-artificial-humans/>

当我们新的电脑霸主到来时，它可能会使用电磁扬声器发出命令(或者更有可能的是，通过发短信而不是说话)。但是对于一个单纯的人造人来说，难道我们不应该使用一个有声带~~和弦~~、鼻腔、舌头、牙齿和嘴唇的人造嘴巴吗？如今这方面的工作很少，但是[马丁·里奇斯]在 1996 年到 1999 年间开发了[一个令人愉快的叫 motor mouth](http://martinriches.de/momomore.html)的东西。

它令人愉快的是它使用了 Z80 处理器和汇编语言，这是我们许多人都记得的东西，还有它的透明侧面板，让我们可以看到工作情况。正如你将在下面的视频中看到和听到的，鉴于这项任务的极端难度，它的效果相当好。

![The lower section with electronics, motors and Bowden cables.](img/fa72904306661345db197c7a7c12c665.png)

The lower section with electronics, motors and Bowden cables.

使用八个步进电机来移动口腔的各个部分，其中七个与电子设备一起位于口腔下方。他们使用[波顿线缆](https://en.wikipedia.org/wiki/Bowden_cable)将电机运动传递到嘴部。其中一个开关阀门，让一些空气流过位于口腔正上方的鼻腔。第八个电机将舌头从口腔的后部旋转到前部，看不到。鼓风机提供空气。与我们人类不同，鼓风机有两条气路。一条路径通过簧片来控制音调，另一条路径可以打开以允许更多的气流绕过簧片。F、S 和 t 等清音需要增加气流。口腔的最前端有两个上下移动的块状部分，一个代表嘴唇，一个代表牙齿。

[Martin 的]网页包括早期的图纸，以及他如何在汇编代码中将八个电机表示为八位的解释。对于可以发出的每种声音，需要启动的电机的相应位被设置，同时还有每个步进电机应该转到哪里以及速度如何的数据。他还提供了一个汇编代码的例子，虽然并不是所有的都在这里。

[https://player.vimeo.com/video/173787687](https://player.vimeo.com/video/173787687)

当我们谈论从零开始制作语音时，不如也从零开始制作 Z80 计算机，就像[Lumir Vanek]用他的[Rum 80 PC](http://hackaday.com/2015/04/15/the-rum-80-a-home-brew-z80-computer-built-from-scratch/)所做的那样。或者你可以像[斯科特·贝克]那样更进一步，不仅为[制造 Z80 计算机，还为它制造语音合成器](http://hackaday.com/2016/09/03/talking-diy-z-80-retrocomputer-complete-with-dev-tools/)。