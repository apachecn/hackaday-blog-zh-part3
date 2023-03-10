# 黑客日奖参赛作品:地震噪音分析设备

> 原文：<https://hackaday.com/2017/05/06/hackaday-prize-entry-device-for-seismic-noise-analysis/>

每当世界上某个地方发生地震时，我们的电视屏幕就会充满地震数据的图像。那些新闻报道图形用简化的小图告知大众，但通常会出错。在这些图像中，总会有一个图表记录器在纸上画出一条重要的地震轨迹，这是很好的电视画面，但可能与地震学的最先进水平相去甚远。

我们不是 Hackaday 的地震学家，所以发现[Michael D]的项目[地震噪音分析设备](https://hackaday.io/project/20735-device-for-seismic-noise-analysis)非常有趣。在这篇文章中，他给出了地震传感器的基本入门，并概述了他对这一主题的看法，这是一种灵敏的宽带地震传感器，旨在捕捉地震背景噪声。似乎许多地震传感器被设计成捕捉大事件，却忽略了它们之间的噪声，使用合适的软件可以从中收集地震事件的预警。

该传感器设计简单，一个质量很大的球放在三个压电麦克风元件上，间隔 120 度。一个阻抗极高的运算放大器电路将来自压电元件的电荷转换并集成为电压，Arduino Yun 可以读取该电压并采集数据。这是一个大胆的主张，但据说该设备已经对田纳西试验场附近的轻微地震事件发出了预警。

地震学以前在这里出现过几次。[这个地震仪使用低音炮作为传感器](http://hackaday.com/2014/12/06/a-web-connected-seismometer/)，而[这个项目使用商业地震检波器](http://hackaday.com/2015/12/01/listening-to-the-sounds-of-the-earth/)，这只是举几个例子。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)