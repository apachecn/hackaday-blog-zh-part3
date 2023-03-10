# 树莓派搭车内复古码头

> 原文：<https://hackaday.com/2017/03/13/raspberry-pi-hitches-ride-inside-vintage-terminal/>

当一次垃圾箱搜寻发现了一个老式视频显示终端时，[dennis1a4]知道该怎么做——让希斯基特 H19 起死回生，并在里面塞一个树莓派。

个人电脑时代的早期是一个市场多元化的时代。每个人都在制造组装完美电脑所需的东西，而终端是最重要的设备之一。李尔西格勒，DEC，Wyse——每个人都参与了这场游戏。就连希思罗机场也与它的 H19 串行终端竞争，这将花费你 1980 年代早期大约一千美元。

[dennis1a4]发现的终端是 DOA，但他很快确定是一个坏的电容短路了-12VDC 轨。需要做一些额外的检测工作，让终端在本地回显字符，并通过 RS-232 端口和 bam(工作终端)输出它们。但是然后呢？树莓派来拯救我们了！但是那些老式的+/-12 伏的波动会给 Pi 带来严重的蓝烟病。在一点点伏特计拨弄之后，通过插座驱动芯片的魔力，Pi 正以令人尖叫的 9600 波特与终端对话，并在 80×24 的单声道显示器上访问 [Hackaday Retro](http://retro.hackaday.com/) 网站。

总而言之，这是对计算机历史的一次很好的破解。但只有一个问题:[它能玩~~末日~~ Flappy Bird 吗？](http://hackaday.com/2017/03/10/flappy-bird-is-the-new-does-it-run-doom/)