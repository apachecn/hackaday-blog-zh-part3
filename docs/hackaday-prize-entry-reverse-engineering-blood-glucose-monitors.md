# Hackaday 奖参赛作品:逆向工程血糖监测仪

> 原文：<https://hackaday.com/2016/07/10/hackaday-prize-entry-reverse-engineering-blood-glucose-monitors/>

血糖监测器如今相当普遍。对于大多数糖尿病患者来说，这些廉价而可靠的传感器是他们管理血糖的主要手段。但是，如果有进取心的糖尿病黑客醒来后惊恐地意识到他日常生活的一个主要方面与 Arduino 无关，他该怎么办呢？

比起屈服于 Arduino-less 现实，他更有希望使用[M. Bindhammer]正在研发的盾牌将他的血糖测量掌握在自己手中。

[Bindhammer]最初的工作是基于流行的一键品牌的条带。这些是最便宜的，用很少的血，并且附带的针头没有想象中的那么糟糕。他面临的第一个挑战是如何获得测试条的连接器。当然，他可以从药房里拆下一个监视器，但是对于一个需要补给线来制造盾牌的人来说，这不是最好的选择。令人惊讶的是，所用的连接器并没有专利，所以这些公司反而对销售对象更加严格。经过一番努力，他设法找到了一个来源。

下一个挑战是对商用传感器使用的实际算法进行逆向工程。很有挑战性。例如，水和葡萄糖的简单混合物会使传感器产生错误。不过，他最终会得到它，这将成为 Hackaday 奖的一个很好的参赛作品。

The [HackadayPrize2016](http://hackaday.io/prize) is Sponsored by: [![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](http://hackaday.io/atmel)  [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](http://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](http://www.digikey.com/)  [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](http://supplyframe.com/)