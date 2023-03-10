# 仅在一种类型的晶体管上的单边带收发器

> 原文：<https://hackaday.com/2018/04/09/an-ssb-transceiver-using-only-one-device-surely-not/>

业余无线电爱好者可以使用多种新旧传输模式，但最主要的还是单边带或单边带。SSB 发射机发射重构音频信号所需的最少 RF 频谱，只有音频和 RF 载波之间混频器乘积的一半，并且载波已被移除。这使得 SSB 成为最有效的模拟语音模式，但代价是需要一个复杂的电路来通过模拟方式产生它。然而，业余无线电爱好者已经为单边带发射机设计了一些优雅的设计，这个来自[VK3AJG]的 80m 波段的设计是一个很好的例子，即使它不是最新的。它的特别之处在于它只依赖于一种类型的器件，它的每个晶体管都是 BC547。

在设计方面，它遵循了其他简单的业余发射机的领先地位，因为它有一个 6 MHz 的晶体滤波器，两端有一个混频器，可以切换发射或接收角色。它没有使用因 [VU2ESE 的 Bitx 设计](https://hackaday.com/2013/11/13/bitx-a-return-to-hackers-paradise/)而流行的双向放大器，而是使用一组二极管开关来选择发射或接收。该功率放大器将单个器件的特性发挥到了极致，将多个 BC547s 并联在一起，可提供约 0.5 瓦的功率。

虽然这个发射机指定 BC547s，公平地说，许多其他设备可以取代这个相当古老的一个。业余无线电爱好者倾向于坚持他们所知道的东西，而 T2 执着于过时的设备，但是在适当的规格范围内，一个给定的双极晶体管与其他双极晶体管非常相似。无论你使用什么设备，这个设计都足够简单，你不需要成为天才就能制造出来。

Via [ [G4USP](http://www.qsl.net/g4usp/BC547%20HF%20TXCVR/All%20transistor%20BC547%20SSB%20HF%20TXCVR.htm) ]。感谢您的提示。