# Hackaday 奖参赛作品:打开啜饮和泡芙

> 原文：<https://hackaday.com/2016/08/31/hackaday-prize-entry-open-sip-and-puff/>

吸喷装置是一种辅助技术，供不能用手的人使用。作为一个准医疗设备，你可以想象这种技术极其昂贵，无法修改，基本上是一个除了设计用途之外什么都不能做的黑匣子。对于他的 Hackaday 奖参赛作品，[Jason]正在[构建他自己的 sip-and-puff 接口](https://hackaday.io/project/12959-opensippuff),它比现有的商业版本更便宜、更强大。

吸喷设备可以被映射来控制轮椅、点击鼠标或按键盘上的键。你可以用 USB 做很多事情，所以对于这个开放式的设备，[Jason]使用的是一直流行的 ATmega32U4 微控制器。

USB 只是问题的一部分，为了测量通过塑料软管吸入和喷出的空气，[Jason]正在使用来自 Freescale/NXP 的压力传感器。虽然这与现成的吸喷设备非常相似，但很难与之交互。当前版本的电路板使用仪表放大器，压力传感器和电路板之间的机械连接略显怪异。[Jason]对更好的传感器有一些想法，在 Hackaday 奖的剩余时间里，他将本着简单的原则重新设计这款设备。

The [HackadayPrize2016](https://hackaday.io/prize) is Sponsored by:[![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](https://hackaday.io/atmel) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://www.digikey.com/) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/)