# Hackaday 奖参赛作品:你可以和一群 NANDs 做任何事情

> 原文：<https://hackaday.com/2016/05/10/hackaday-prize-entry-you-can-do-anything-with-a-bunch-of-nands/>

每隔几年，互联网上就会有人造出真正的自制 CPU。也不是用 6502、Z80 或 80 年代的 CPU 构建的:完全用 74 系列逻辑芯片或分立晶体管构建的。我们很幸运有[Alexander]在 Hackaday.io 上记录他的构建，更幸运的是让他参加今年的 Hackaday 奖。这是一台完全由与非门构成的 8 位计算机。

计算机只是逻辑，有了足够多的与非门，你可以做任何事情。这正是[亚历克斯]在这台电脑上所做的。它完全由 74F00 芯片构建而成，是无处不在的四路 2 输入 NAND 芯片的“快速”版本。这台电脑的结构借鉴了 70 年代和 80 年代最好的中央处理器。ALU 只有 4 位，像 Z80 一样，但也使用 6502 技术，借位是反向进位。这是一个小指令集，两级流水线，每秒应该能够计算一百万条指令。

设计一个 CPU 是一回事，多亏了 Logisim，这个已经完成了。构造一个 CPU 完全是另一回事。为此，[Alex]将采用模块和背板的方法，其中 ALU 由几个相同的模块连接在一起构成一个巨大的主板。[Alex]也没有停留在 CPU 上:他有一个 16 字节的 ROM[，通过将二极管插入孔中](https://hackaday.io/project/9795-nedonand-homebrew-computer/log/35219-board-nedonand-16-tested)来编程。

这是一个令人惊讶的雄心勃勃的项目，因为这个项目进入了 2016 年 Hackaday 奖，[Alex] [已经为自己赢得了 1000 美元](http://hackaday.com/2016/05/02/these-20-projects-won-1000-in-the-hackaday-prize/)和一次参加最后一轮比赛的机会。

The [HackadayPrize2016](http://hackaday.io/prize) is Sponsored by: [![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](http://hackaday.io/atmel)  [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](http://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](http://www.digikey.com/)  [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](http://supplyframe.com/)