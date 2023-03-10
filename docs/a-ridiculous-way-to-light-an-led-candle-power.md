# 点亮 LED 的荒谬方式:烛光

> 原文：<https://hackaday.com/2016/03/30/a-ridiculous-way-to-light-an-led-candle-power/>

如果你曾经通过阅读全面的电子理论教科书自娱自乐，你会看到一些听起来很有趣但你很少会拿在手中的技术参考。它们可能是已经被最近的创新所取代的死胡同，或者它们可能是已经找到用途的技术，但是在它们最初显示出希望的领域的其他领域。如果你能把这些疯狂的部分真的造出来呢？

[Fedetft]有一个有趣的项目，结合了两个有趣的教科书参考文献，[他创造了一个热电堆，通过逆变器点亮 LED，逆变器的振荡器是隧道二极管](https://fedetft.wordpress.com/2016/03/25/thermopiles-and-tunnel-diodes-a-candle-powered-led)。翻出课本。

如果你用过热电偶温度计或半导体热电发电机，那么你会遇到[热电效应](https://en.wikipedia.org/wiki/Thermoelectric_effect)。也许你甚至在这种模式下操作过珀耳帖制冷元件。当电路由不同类型的导体之间的两个结构成，并且两个结之间存在温差时，电路中会有电流流动，该电流取决于温差的大小和导体的特性。

热电堆是金属导体之间的这些热电结电路的集合，串联排列以增加电压。[Fedetft]的热电堆使用取自 [K 型热电偶](https://en.wikipedia.org/wiki/Thermocouple#Type_K)的镍铬合金和铝镍合金线。他做了六组接点，并用小云母片支撑它们。利用蜡烛的热量，他发现可以产生大约 200 毫伏的电能，大约 3.7 兆瓦。

[![The RCA tunnel diode inverter circuit](img/a84fb8a56650ba8a3994f546f509e0cc.png)](https://hackaday.com/wp-content/uploads/2016/03/tunnel-diode-circuit.jpg)

The RCA tunnel diode inverter circuit

如此微小的电力来源对于直接点亮 LED 几乎没有用处，所以他需要制造一个逆变器。这就是[隧道二极管](https://en.wikipedia.org/wiki/Tunnel_diode)的用武之地。隧道二极管具有负阻区，可用于在极其简单的电路中以极高的频率放大和振荡，但在 2016 年，这种器件并不常见。[Fedetft]有一个俄罗斯隧道二极管，他在 1963 年的 [RCA 隧道二极管手册中找到的逆变电路中使用了环形变压器。这是一个双组分](https://archive.org/details/RcaTunnelDiodeManual)[焦耳小偷](https://en.wikipedia.org/wiki/Joule_thief)。对于那些对隧道二极管感兴趣的人来说，RCA 手册本身就是一本很好的读物。

由此产生的电路产生峰值为 4.5v 的 15kHz 振荡，其功率刚好足以点亮一个 LED。

虽然仅仅用明亮的蜡烛点亮 LED 似乎毫无意义，但[Fedetft]项目的重要部分是从教科书中获得对这两种落后技术的一些理解。我们对此表示赞赏。

这是一项真正深奥的技术的标志，它在 Hackaday 上很少出现，这两者都不会令人失望。[我们只是顺便提了一下隧道二极管](http://hackaday.com/2012/05/17/a-bit-more-about-the-diode/)，在一般情况下，我们倾向于使用“热电堆”[在另一种意义上指代热成像相机](http://hackaday.com/tag/thermopile/)。