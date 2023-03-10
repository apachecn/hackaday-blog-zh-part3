# 平方英寸项目

> 原文：<https://hackaday.com/2015/12/11/the-square-inch-project/>

在过去的几年里，Hackaday 组织了一些令人惊叹的比赛。我们送出了一次太空之旅，但获胜者却拿走了钱。我们又送出了一次太空之旅，但那些获胜者却拿走了钱。但是我们一路上玩得很开心，很高兴看到其他人也加入进来。9 月，hackaday.io 上突然出现了一场竞赛，这就是平方英寸项目(Square Inch Project),比赛的目标是在一平方英寸的印刷电路板上塞入最多的电子器件。

这不是一场由这里的任何负责人设计、策划或组织的比赛；这是一场完全有机的比赛，由 [hackaday.io](https://hackaday.io) 社区安排和实施。几个月前，一些著名的 hackaday.io 人*刚刚决定*举办一场比赛。太棒了。

OSHPark 非常好心，给多氯联苯的积分作为奖励，我们在 Hackaday 商店增加了一些礼券。显然，这就是让很多人做出很多很酷的东西所需要的一切。

有很多非常棒的条目——太多了，一篇帖子无法涵盖——但是你可以在下面找到一些很棒的条目。

 [![OSHchip](img/e761302373879d437ac2093f1dbabae1.png "OSHchip")](https://hackaday.com/2015/12/11/the-square-inch-project/oshchip-2/)  [![Word Clock](img/ce2d5f0da8f64886e74f8dcb7343ce85.png "Word Clock")](https://hackaday.com/2015/12/11/the-square-inch-project/word-clock-2/) 

[Peter]对蓝牙开发平台有一个有趣的想法。它具有实际的调试能力，完全标准化，并提供电路板封装。该芯片是一个 nRF51822，一个内置蓝牙的 ARM Coretex M0。它的尺寸与 16 引脚 DIP 相同，使开发变得容易。任何人所要做的就是将 OSHChip 放入一个无焊的试验板中，接上电源，编写使用蓝牙的有趣应用程序。

单词钟——代替数字或表盘来拼写时间的钟——已经存在了大约十年。他们的结构其实很简单，只是一个 LED 阵列和一个字母的面具。通常字钟很大，但是 8×8 LED 矩阵已经存在很久了。【丹尼尔·罗哈斯】把两个和两个放在一起，创造了[微型字钟](https://hackaday.io/project/7961/)。该板约为 0.79 英寸，包含一个 ATMega328、一个 DS1307Z+实时时钟，其他内容不多。一个 8×8 字母的网格比传统的单词钟小得多，这意味着在一些单词中间有一些奇怪的空格。它看起来仍然很棒，这是一个很好的例子，说明一平方英寸可以容纳多少东西。

[![9260631446661683100](img/1ad0226457f9b39337f130713c032e3e.png)](https://hackaday.com/wp-content/uploads/2015/12/9260631446661683100.jpg)

led 的颜色不仅仅是红色、绿色和蓝色。市面上有各种各样的糖果色 LED，如果你非常勤奋地阅读数据手册，你可以买到任何波长的 LED。Rohm 的 PICOLED 系列 LED 有 14 种不同的颜色，哪里有 led，哪里就有 blinkey 玩具。[zakqwy]想要一个 blinkey 的彩虹，最终建造了[rrrrrooyyyyyggbgbpw Blinktronicator](https://hackaday.io/project/8331-rrrrooyyyygygggbgbpw-blinktronicator)。对于一个将小 PCB 变成彩虹的项目来说，这是一个可怕但准确的名字。不包括独角兽。

 [![Nyan](img/07efc923ff1feb27b589f47a6b5f747c.png "Nyan")](https://hackaday.com/2015/12/11/the-square-inch-project/nyan-5/)  [![Numitron clock (discussed below)](img/fb631211e21cca8be73d84f143158a64.png "numitron")](https://hackaday.com/2015/12/11/the-square-inch-project/numitron-3/) Numitron clock (discussed below)

说到彩虹，[拉多米尔]用一只流行蛋挞猫建造了一个最纯粹的彩虹的例子。这是一个 nyan 板，或 Nyan 猫人格化。这个小电路板的形状像每个人最喜欢的家养毛猫，包含几个用于眼睛的 blinkey LEDs，一个 ATtiny 微控制器和一个扬声器。当彩虹带状电缆插入电源时，扬声器播放 nyan cat 主题曲。你可以[查看 nyan 板运行的视频](https://www.youtube.com/watch?v=0jn2UKNfeAQ):

 [https://www.youtube.com/embed/0jn2UKNfeAQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/0jn2UKNfeAQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



微板需要微电子和小电池，但并不总是如此。[Jeremy]正在建造一个只有一个电子管的钟。当然，单芯片数码管驱动器对于一个平方英寸的项目来说太大了，因为它还需要微控制器、实时时钟和某种电源。幸运的是，移位寄存器封装非常小。时钟由 400mAh 的 LiPo 电池充电供电。RTC 使用一个 300 兆赫兹的超级电容来防止它失去理智。这里有一个时钟运行的视频:

 [https://www.youtube.com/embed/B9-GcfNA68Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/B9-GcfNA68Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



时钟和闪光灯是一回事，但完整的视频游戏机完全是另一回事。把它塞进一平方英寸是一个了不起的成就。这就是[rossumur]在他的 Arduinocade 项目中所做的[。这个项目使用一个运行在 28.6363 MHz(NTSC 载波频率的倍数)的微控制器来玩类似 PacMan、Joust 和一个奇怪的伪 3D 网球游戏的游戏。用来从这个小芯片(和微型板)中挤出性能的视频技巧非常令人印象深刻。这就是它之前收到自己的帖子](https://hackaday.io/project/7666-arduinocade)的原因。

控制输入是通过一个红外操纵杆，虽然这个项目需要一个试验板来进行所有的连接，弯曲了平方英寸项目的规则，但这不是一个小的适配器板不能解决的问题。

 [https://www.youtube.com/embed/nGIujZiEu_o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/nGIujZiEu_o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



* * *

平方英寸竞赛之所以有趣，是因为它完全是 hackaday.io 社区的有机产物。毫不夸张地说，有一天，一些人决定在 hackaday.io 上再举办一场比赛。该网站注册人数超过 10 万人，有足够多的参赛作品供平方英寸的评委审核。