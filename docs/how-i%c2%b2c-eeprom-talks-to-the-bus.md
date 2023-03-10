# I C EEPROM 如何与总线通信

> 原文：<https://hackaday.com/2016/09/01/how-i%c2%b2c-eeprom-talks-to-the-bus/>

您可能对 I C 很熟悉，这是一种串行总线，通常用于与微控制器外设进行速度不是很快的通信。不过，很可能除非你是一个 I C 奇才，否则你不会对其错综复杂的操作非常熟悉，而且每一个新设备都将带来一段研究数据表和挠头的漫长时间。

如果前一段描述了你，请继续读下去。[ Clint Stevenson]编写了一个用于 I C EEPROMs 与 Arduino 平台接口的库，当一个用户在 ATtiny85 上使用它时发现了一个 bug，他写下了他的解决方案。[由此产生的一篇文章清楚地解释了 I C EEPROMs 如何与总线](http://www.cascologix.com/blog/interfacing-with-i2c-eeprom)通信，你可以对它们执行的各种操作，以及总线上每个地方的开销。然后，他继续解释 EEPROM 时序，以及由于器件执行每项任务需要一段时间，微控制器必须确保任务完成后才能执行下一项任务。

在[Clint]的库的例子中，问题被证明是在处理 I C 启动条件时与 Arduino Wire 库不兼容。I C 有一个时钟和一条数据线，当没有任务执行时，两者都为高电平。起始条件向总线上的器件指示即将发生什么，当时钟线保持高电平一段时间后，数据线变为低电平，然后时钟线启动，数据线携带 I C 命令。他在上面链接的页面上发布了代码样本，你可以在他的 GitHub 库中找到他的库[。](https://github.com/CascoLogix/CAT24M01)

如果你想更多地了解 I C，看看 Hackaday Editor[埃利奥特·威廉姆斯]关于这个主题的大师班:[什么可能出错，I C 版](http://hackaday.com/2016/07/19/what-could-go-wrong-i2c-edition/)，以及[嵌入 Elliot，I C 总线扫描](http://hackaday.com/2015/06/25/embed-with-elliot-i2c-bus-scanning/)。

串行 EEPROM 芯片图片，由 Epop(自有作品)[CC0]，通过[维基共享](https://commons.wikimedia.org/wiki/File:ATMEL048_93C46A_SC.jpg)。