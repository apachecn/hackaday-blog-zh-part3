# Hackaday 奖参赛作品:毫微微蜂窝中继器

> 原文：<https://hackaday.com/2017/05/13/hackaday-prize-entry-a-femtocell-repeater/>

为了获得 Hackaday 奖，【tegwyntmmffat】[正在建造一个手机信号中继器](https://hackaday.io/project/20500-cell-phone-signal-repeater-booster-femtocell)。这种设备可以在市场上买到，但要么价格昂贵，要么明显不符合射频法规，有些设备在 DealExtreme 上售价 30 美元。该项目旨在创造一种经济高效、可破解的设备，能够正常工作并符合正确的法规。

该系统的核心是 LimeSDR 收发器。[这是我们在](http://hackaday.com/2016/07/29/the-problem-with-software-defined-radio/)之前见过的一块板，它有几个有趣的特性。基本上，LimeSDR 的核心是一个可编程的 RF 收发器，覆盖范围从 100kHz 到 3.8GHz。还有片内信号处理和 USB 3.0 带宽，可以将信号发送到计算机或从计算机接收信号。

现在，[tegwyntmmffat]的重点是让他的 LimeSDR 运行起来，并弄清楚如何建立几个无线电模块来做需要做的事情。项目[有一个很好的更新，展示了坑洞](https://hackaday.io/project/20500-cell-phone-signal-repeater-booster-femtocell/log/57456-limesdr-test-limesuite-was-used-to-scoop-up-settings-generated-by-pothos)，到目前为止【Tegwyn】有一个全双工中继器在工作。这是一项伟大的工作，真正展示了软件定义无线电的能力。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)