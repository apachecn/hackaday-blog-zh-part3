# Tiny-TS:一个可玩的 Synethesiser 能有多小？

> 原文：<https://hackaday.com/2016/12/11/tiny-ts-just-how-small-can-a-playable-synethesiser-get/>

早期的电子合成器是巨大的机器，装满整个房间的电子模块架。随着时间的推移，电子产品的集成不断缩小它们，首先缩小到一件大型家具的大小，然后缩小到桌面控制台、独立键盘和从另一种乐器或电脑接收指令的小型 MIDI 黑匣子。最初大量的分立电子器件被简化为一堆集成电路，然后是芯片组，最后是单个集成电路和微型计算机上的软件实现。

因此，现在有可能制造一个相当小的合成器。如果你能在里面安装一个微控制器，你就能在里面安装一个合成器。但是一个*可玩的*合成器怎么样？一个有键盘的，你可以在上面举行独奏会？你能做多大的？[Jan Ostman]凭借他的 Tiny-TS(T2)赢得了最小可播放合成器奖，这是一款带有一个八度电容键盘和合成参数模拟控制的信用卡合成器。

合成器的核心是 ATMega328，他为其提供软件。可通过一系列电位计调整的参数如下所示:DCO:粗音高和双倍，DCF:滤波器峰值和包络 mod，以及包络:影响振幅的起音和释音。你可以建造自己的，或者他告诉我们，如果你想买一个现成的，他会把这个项目作为 Kickstarter 活动。

如果你想知道，这听起来并不太糟糕。一些极简合成器牺牲了他们可以创造的声音的广度，但不是这个。他在 YouTube 视频中测试了它的速度，我们把它放在了休息时间下面。

 [https://www.youtube.com/embed/m7zQsG0H94w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/m7zQsG0H94w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



电子音乐以前在这里出现过很多次，但特别的是，我们给你带来了一些微型合成器。突出的是[Jan]以前的项目，他的 MIDI 插头中的[MIDI synth](http://hackaday.com/2016/03/30/the-attiny-midi-plug-synth/)和他的[单片罗兰 808 鼓机](http://hackaday.com/2016/09/28/808-drum-machine-in-an-attiny-14-pin-chip/)。