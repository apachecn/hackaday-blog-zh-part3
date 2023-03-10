# Hackaday 奖参赛作品:脑电图检测癫痫发作

> 原文：<https://hackaday.com/2017/05/02/hackaday-prize-entry-eeg-seizure-detection/>

对于那些患有癫痫的人来说，癫痫发作是一件危险的事情。除了对神经系统的影响，周围环境也有可能造成伤害——想想在繁忙的道路附近癫痫发作的危险，甚至只是一张玻璃桌子。对于癫痫发作患者存在一些检测方法，但是它们主要基于检测患者的抽搐运动。[akhil2001us]认为有可能做得更好–[通过测量脑电波来检测癫痫发作](https://hackaday.io/project/21385-neurowave-seizure-detection-device)。

构建围绕 [Neurosky Mindwave 耳机](https://store.neurosky.com/pages/mindwave)展开。这是一个现成的产品，专为捕捉脑电图数据而设计。它输出原始脑波数据，这是进行适当分析的关键。该项目然后使用 Arduino Mega 将所有东西联系在一起，同时使用一些 Sparkfun 蓝牙模块与手机通话，在癫痫发作时发送短信求助。

像这样一个项目的真正困难来自于开发一种能够可靠地检测癫痫发作的算法，以及一种足以在现实世界中工作的强大单元。如果你的耳机正在检测癫痫发作，这是没有用的，但帮助信息永远不会发送，因为一根电线从你的试验板上掉了下来。正是出于这样的考虑，再加上诉讼的威胁，医疗设备才被如此严格地设计和认证。然而，对于概念验证来说，这种担心并不重要。

我们已经看到了之前的[思维波——脑波研究是一个令人兴奋的领域！](https://hackaday.com/tag/mindwave/)

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)