# hack let 123–手表

> 原文：<https://hackaday.com/2016/09/03/hacklet-123-watches/>

时间不等人。乔叟可能是对的，但是一个戴着手表的男人(或女人)可以在时间悄悄接近他们之前领先一步。然而，人们永远不会仅仅满足于时间。他们想要日期，月亮的相位。[沃兹]总结得很好，他说“我想要整个智能手机，整个互联网，都在我的手腕上”。黑客也喜欢手表，这意味着有很多手表项目。有些甚至会报时。本周我们来看看 [Hackaday.io](https://hackaday.io) 上一些最好的手表项目！

[![chronio](img/32f5e591f3dcb1337b1c996a5ba7882f.png)](https://hackaday.io/project/12876-chronio) 我们从【Max。K]和[编年史](https://hackaday.io/project/12876)。你可能会认为 Chronio 看起来有点像 Pebble Time，你是对的！[Max]他的设计主要基于 Pebble 的外壳设计。Pebble 甚至在 GitHub 上有他们的 CAD 文件，这有助于[Max]修改他的 3D 打印版本。Chronio 基于 Arduino，使用带有 Arduino 引导程序的 ATmega328p 微控制器。显示器是夏普的 96×96 像素内存 LCD。DS3231 保持时间准确，并提供一个免费的温度传感器。整个手表由 CR2025 电池供电。运行 20uA 睡眠电流，[Max]估计这款手表在一块电池上可以使用大约 6 个月。

[![neopixel-pocket](img/736809e472db2854a9ee4873ad9170ba.png)](https://hackaday.io/project/13353) 接下来我们有【约书亚·斯奈德】和[尼奥像素怀表](https://hackaday.io/project/13353)。谁说手表必须戴在手腕上？[约书亚]给派对带来一些蒸汽朋克风格。他的手表使用 Adafruit 12 NeoPixel 戒指来显示时间。红色、蓝色和绿色的 LEDS 代表时针、分针和秒针。手表由 ESP8266 控制。时间通过 WiFi 设置。在 led 和耗电的 ESP8266 之间，这不完全是低功耗设计。不过，150 毫安时的 LiPo 电池应该可以让系统运行几个小时。这些时间足够在下一次黑客空间活动中引起轰动。

[![pi-watch](img/8e336827df6883b116b3a04e3cbdc01f.png)](https://hackaday.io/project/3666) 接下来是【ipaq3115】和[Pi 手表](https://hackaday.io/project/3666)。圆形智能手表为圆形液晶显示屏创造了一个市场。这些屏幕已经开始渗透到黑客/创客市场。[ipaq3115]得到了一个，必须用它设计一些很酷的东西。Pi 手表不是由覆盆子 Pi 驱动的，而是一个小小的 3.1。[ipaq3115]在他自己的定制板上包括 Freescale/NXP Kinetis 处理器和 MINI54 bootloader 芯片。他使用 Teensy 的模拟输入创建了自己的 10 元素电容式触摸环。这款手表甚至还有一个 LSM303 磁力计/加速计。然而，所有这些力量都是有代价的。它需要一个 480 mAh 的 LiPo 电池来保持 Pi 手表的运行。

[![vikas](img/6e4afb230392bfec7031c40c21b990e3.png)](https://hackaday.io/project/5511) 最后我们还有【Vikas V】和[滚动观看](https://hackaday.io/project/5511)。谁说手表一定要有液晶的？[Vikas V]想要在他的手腕上安装一个滚动 LED 显示屏，所以他自己做了一个。一个 Atmel ATmega88V-10AU 控制一个 16×5 的 charlieplexed LED 阵列。[Vikas]包含了 flash 中许多 ASCII 符号的字符字体，因此这款手表可以显示信息。电源来自定制 PCB 安装支架中的 CR2032 手表电池。[Vikas]目前最大的问题是 LED 之间的漏光。他正在考虑将阵列安装在手表底部。通过 PCB 上的孔向上照射 led 肯定会有助于减少漏光。

如果您想查看更多手表项目，请查看我们新的[手表项目列表](https://hackaday.io/list/13414-watch-projects)。注意到我可能错过的一个项目吗？不要害羞，[在 Hackaday.io 上给我留言就行了](https://hackaday.io/adam)。这就是本周的 Hacklet，一如既往，下周见。同样的黑客时间，同样的黑客频道，带给你最好的 [Hackaday.io](https://hackaday.io/) ！