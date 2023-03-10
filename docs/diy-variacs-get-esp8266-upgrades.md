# DIY 自耦变压器获得 ESP8266 升级

> 原文：<https://hackaday.com/2018/05/14/diy-variacs-get-esp8266-upgrades/>

如果你从事黑客和制作的时间足够长，你可能会遇到这样的情况:你意识到以前的项目可以通过添加技术来改进，而这些技术在你构建它时根本不可用。有时这意味着从头开始，但偶尔你运气好，可以硬塞进一些新装备，而不必回到绘图板。

[![](img/4a99135f3cd96690a9f024dfa35b929f.png)](https://hackaday.com/wp-content/uploads/2018/05/espvariac_detail.jpg)【nop head】制造的两个隔离自耦变压器已经令人印象深刻，但[随着 ESP8266 的加入，他能够添加一些非常巧妙的附加功能](http://hydraraptor.blogspot.com/2018/04/esp8266-spi-spy.html)，这真正将它们带到了一个新的水平。他做了出色的工作，详细介绍了新的修改，包括为任何可能走在类似道路上的人提供所有源代码。

他的自耦变压器的前面板上有数字电表，可以给出电压、电流和瓦特的实时计算结果。在阅读了[Thomas Scherrer]的一篇关于用 Arduino 从这些仪表中嗅出 SPI 数据的文章后，[nop head]推断他可以用 ESP8266 做同样的事情。这样做的好处是，他可以通过网络将数据提取出来，然后按照自己的意愿绘制图表或进行分析。

对于他的老款 variac，他决定通过添加步进器和皮带来转动旋钮，从而实现设备的自动化。步进机由 Pololu 步进机驱动器控制，该驱动器又从另一个 ESP8266 获得其行进指令。他甚至想出了一个简单的网络界面，允许你从智能设备上监控和控制自耦变压器。

我们很少在这些部件周围看到很多[自耦变压器，甚至更少尝试](https://hackaday.com/2017/09/09/things-learned-from-hot-wire-cutting-a-droids-body/)[制造定制的](https://hackaday.com/2016/05/15/taming-a-variac-with-a-thermistor/)。这是一种你没有 T5 就无法生活的[设备，或者是你从未听说过的设备。](https://hackaday.com/2017/10/13/what-tools-do-you-reach-for-first/)