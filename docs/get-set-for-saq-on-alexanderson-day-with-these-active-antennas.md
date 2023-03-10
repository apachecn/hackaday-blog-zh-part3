# 使用这些有源天线，为亚历山大日的 SAQ 做好准备

> 原文：<https://hackaday.com/2016/06/26/get-set-for-saq-on-alexanderson-day-with-these-active-antennas/>

如果需要产生射频电信号，就要制作某种形式的电子振荡器。我们可能都习惯于使用晶体管、电子管、逻辑门或许多其他电子技术的振荡器。同样，如果你需要产生高功率的无线电频率，你可以将振荡器耦合到放大器，这对于今天的电子零件箱来说是一个相对简单的任务。

如果你需要在 20 世纪初用高功率无线电信号做同样的事情，这些选项都没有对你开放。没有晶体管或集成电路，当时的电子管无法产生高功率输出。当时的无线电工程师不得不采用其他方法来解决这个问题，其中之一就是亚历山大交流发电机。这是我们之前在 Hackaday 报道过的[旧闻，这是一种能够在 VLF 无线电频率范围内产生数百千瓦功率的高频交流发电机。](http://hackaday.com/2015/06/27/the-alexanderson-transmitter-very-low-frequency-radio-rides-again/)

世界上还有一台 Alexanderson 交流发电机在瑞典 Grimeton 的 Varberg 无线电台运行。它不再经常使用，但作为世界遗产和博物馆，它每年都会播出几次，包括最接近 7 月 2 日的周日，即众所周知的[亚历山大日](https://en.wikipedia.org/wiki/Alexanderson_Day)。我们现在来看这篇文章的要点:今年的 7 月 3 日[亚历山大日传输很快就要到来](http://alexander.n.se/reminder-of-grimeton-radiosaq-transmission/)，自从上次我们报道它以来，我们已经结束了一个良好的甚低频天线设计的请求，我们应该及时发布一个解决方案，让我们的读者能够接收到今年的信号。

[![G3XBM's e-field VLF antenna](img/a6ab0898c9e8c51d8887e2de250a1b5f.png)](https://hackaday.com/wp-content/uploads/2016/06/efp.jpg)

[G3XBM’s e-field VLF antenna](https://sites.google.com/site/g3xbmqrp3/antennas/efp)

安装一个接收器非常简单，我们在之前的报道中链接了原始的 [SAQrx VLF 接收器](https://sites.google.com/site/sm6lkm/saqrx/)和[扩展版本](https://sites.google.com/site/swljo30tb/)。这两个软件都使用计算机的声卡作为软件定义无线电的前端，以接收来自 Grimeton 的 17.2kHz。但是天线存在一个问题。你可能认为在麦克风输入端连接一根长电线就足够了，但问题是，由于 VLF 信号的波长很长，你可能能够组装的任何合理的长电线都不够长，无法提供良好的效果。显然，需要不同的天线，而高阻抗有源电场天线是解决方案。它使用一个 FET 输入和一个非常小的贴片天线，在 VLF 频率下提供低本底噪声，而不是您可能期望的放大器。

我们找到了几个设计供你参考。第一个是[双晶体管版本，你可以在许多网站上找到各种不同的伪装](https://sites.google.com/site/g3xbmqrp3/antennas/efp)。该器件使用 MPF102 FET，但您可以用 J310 替代。第二个设计更令人惊讶，[虽然它是 FET 输入放大器的相同想法，但它使用 TL071 运算放大器作为其有源器件](http://dl1dbc.net/SAQ/homebrew_e-field.html)。这绝不是你通常期望在 RF 电路中找到的 IC，然而，所讨论的频率不是你的正常 RF 的频率。

如果你建造了这两个天线中的任何一个，我们希望你能听到亚历山大森日传输。大功率甚低频发射机的优点是覆盖范围大，因此可以接收到整个欧洲，甚至美国东部的信号。如果你在范围之外，不要害怕。你总是可以试着通过离信号源更近的一个方便的 [webSDR 接收器来接收它。](http://websdr.ewi.utwente.nl:8901/)

Alexanderson 交流发电机图片由 Gunther Tschuch(自己的作品)[ CC BY 2.5 ]，通过[维基共享](https://commons.wikimedia.org/wiki/File:Alexanderson_Alternator.jpg)。