# Prusa 发布 4 台挤出机升级版

> 原文：<https://hackaday.com/2016/09/28/prusa-releases-4-extruder-upgrade/>

我们来谈谈桌面 3D 打印机上的多材料打印。用一种以上的颜色打印会有很多问题。做到这一点最简单的方法是简单地添加另一个挤出机和热端至打印机，但这减少了构建体积，增加了打印机不需要更多质量的部分的质量，并且确保每个喷嘴处于正确的 Z 高度是困难的。多种材料印刷的最佳解决方案是某种混合加热，只从一个喷嘴喷出塑料，由鲍登系统供给。

【Prusa】是人，不是打印机，[刚刚发布了 Prusa i3 mk2](http://prusaprinters.org/original-prusa-i3-mk2-multi-material-upgrade-release/) 的多材质升级版。这次升级允许 i3 mk2 仅使用一台 hotend 打印四种颜色，并且允许任何人将他们的打印机变成多材料发电站。

这种多材料升级背后的基本思想是一个四向 Y 形灯丝路径。每种颜色的细丝被装入一个单独的挤压机中，当材料改变时，当前“活动”的细丝从加热器中缩回，刚好在细丝路径交叉之前。在热端中交换灯丝后，先前灯丝颜色的剩余部分被喷射到一个小(3x5cm)塔上。

因为这是对 i3 mk2 的升级，Prusa 需要一种方法来添加三个额外的步进电机，而不必更换打印机的电子板。他使用基于 SSR 的多路复用器来实现这一点，该多路复用器允许一个步进电机输出和几个 GPIOs 来控制四个电机。

如果你有一台 i3 mk2，你的打印机的四种材料升级将在几个月后以 249 美元的价格上市。这意味着一台全彩色四挤出机 i3 mk 2 的成本不到 1000 美元，这是其他多材料打印机无法企及的价格。

你可以看看下面[Prusa 的]多材质升级的视频。打印机和人将在美国参观 Maker Faire 和开放硬件峰会，你可以打赌我们会得到一些这种多材料打印机的视频。

 [https://www.youtube.com/embed/KpcH74DXyy0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/KpcH74DXyy0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

