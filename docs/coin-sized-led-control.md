# 硬币大小的 LED 控制

> 原文：<https://hackaday.com/2017/09/05/coin-sized-led-control/>

EE 和固件开发人员[Enrico]小时候玩过 led，由于施加了太多的电流而烧坏了它。得益于他的固件印章，他着手[创建一个正确驱动 led 的电路板](https://enricosanino.wordpress.com/2016/06/14/tiny-robust-low-cost-fail-safe-led-driver-the-glighter-s-project/)。

[Enrico]的项目围绕德州仪器 LM3405 降压控制器展开。它接受从 3V 到 20V 的任何输入电压，并向一个或多个 led 输出高达 20V/15W 的电压。他内置了大量的安全功能，如短路和开路免疫、温度控制和空闲时自动关闭开关。他还创建了一个 LED 板来测试驱动器的最大效率。它由四个 Luxeon Rebel ES 二极管组成，RGB 和 w 各一个。LED 板的整个背面是铜的，附有一个巨大的散热器。

你可以跟随 Hackaday.io 上的 [Glighter-S 项目](https://hackaday.io/project/12245-glighter-s)，或者你可以[从他的 Tindie 商店买一块他的主板](https://www.tindie.com/products/thexeno/glighter-20w-tiny-led-driver/)。

我们过去已经广泛地讨论过 LED 驱动器，有关于简单的 10 瓦 LED 驱动器的文章和关于如何设计自己的 LED 驱动器的文章。