# Hackaday 奖参赛作品:鹿——一种电子驱虫剂

> 原文：<https://hackaday.com/2017/05/29/hackaday-prize-entry-deer-an-electronic-repellent/>

用于驱赶昆虫、啮齿动物、鸟类甚至大型动物的超声波驱虫器已经存在了相当长一段时间，但它们的有效性取决于你问的是谁。一些动物似乎并没有受到影响，而其他一些动物肯定会避免出现在这样的设备周围。部署一些这样的装置来吓跑动物似乎对[ondřej·佩特里克]很有效。在他居住的地方，春天的时候需要割草。不幸的是，高草是幼小新生动物藏身和安全的理想场所。割草机器经常会使这些动物致残或受伤，[Ondřej]急切地想解决这个问题并防止这些事故的发生。

他在捷克共和国的农场/牧场/牧场建造了一个电子驱虫器来驱赶野生动物和它们的后代。他用一个 Arduino Mini 来驱动一个大型压电传感器，以吓跑设备附近的野生动物。他可能使用了超出人类范围的足够高的频率，但当他公布他的代码和细节时，我们会知道更多。还有几个 10 毫米大的 LED——要么在视觉上定位设备，要么结合超声波帮助驱赶动物，LDR 在晚上激活 LED。使用 Arduino 有助于以随机间隔打开传感器，希望他使用的是一系列不同的频率，这样动物就不会对该设备产生免疫。

他的第一个原型是用现成的香草零件拼凑而成的。一个 Arduino，一个升压转换器，一个 LDR，几个 led，一个通过磁铁供电的簧片开关，以及一个大型超声波换能器，所有这些都由三节碱性 a a 电池供电。他把所有东西都塞进一个防风雨的模制外壳里，用大量的热胶水把它们粘在一起。这并没有使它在长期的户外使用中变得非常坚固。虽然原型运行良好，但他需要在他的农场周围放置几个设备。为了使组装更容易，更可靠，他设计了一个定制的 PCB，以适应全天候的外壳。这使他能够轻松地安装所有需要的部件，以获得更可靠的结果。他的项目仍在进行中，所以如果你使用过这些类型的超声波驱虫器来驱赶动物，并且有任何可能帮助他的见解，请发表你的评论。[Ondřej]似乎对目前的结果相当满意。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)