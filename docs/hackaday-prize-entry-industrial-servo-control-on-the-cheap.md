# 黑客日奖参赛作品:廉价的工业伺服控制

> 原文：<https://hackaday.com/2016/05/23/hackaday-prize-entry-industrial-servo-control-on-the-cheap/>

[Oscar]想知道为什么业余爱好项目[忽略了所有功能强大的无刷电机](https://hackaday.io/project/11583-odrive-high-performance-motor-control)，其价格远低于同等的步进电机，特别是用先进的技术来克服[他们的不足](http://hackaday.com/2016/02/23/anti-cogging-algorithm-brings-out-the-best-in-your-hobby-brushless-motors/)。他认为这肯定是因为没有一个好的、便宜的、开源的电机控制器来精确地驱动它们。所以，他做了一个。

步进电机很适合它们所做的事情，沿网格开环定位，但就工业电机而言，它们真的不是最好的技术。步进器因制造简单和易于控制而在成本曲线上胜出，但当涉及到高端自动化时，它始终是伺服控制。电机功能更强大，闭环控制也更精确，但它们需要更多的控制逻辑。[Oscar]的主板旨在填补这一空白，并充分利用这一电机控制技术。

对于目标价格低于 50 美元的产品，董事会可以做一些令人印象深刻的事情。它支持两个 24 伏的电机，峰值电流高达 150 安培。它可以采用编码器输入进行全闭环控制。它支持电池再生制动。您甚至可以通过添加锂电池来增加一个更适中的电源，以允许偶尔的 1 KW 峰值移动。休息之后，您可以在视频中看到该板展示了它的一些功能。

 [https://www.youtube.com/embed/WT4E5nb3KtY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/WT4E5nb3KtY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2016](http://hackaday.io/prize) is Sponsored by: [![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](http://hackaday.io/atmel)  [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](http://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](http://www.digikey.com/)  [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](http://supplyframe.com/)