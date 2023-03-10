# Hackaday 奖参赛作品:极简 Z80 电脑

> 原文：<https://hackaday.com/2017/10/26/hackaday-prize-entry-the-minimalist-z80-computer/>

最好的项目似乎总是来自易贝。几周前，我们发现了一些用于巨型 LED 面板安装的瓷砖，50 美元可以买到 10 块瓷砖。易贝拍卖会现在已经卖完了。不久前，[ [Just4Fun](https://hackaday.io/Just4Fun) ]意识到他可以用每个人都喜欢的网上拍卖行价值 4 美元的零件组装一台 Z80 微型电脑。[结果是一台价值 4 美元的 Z80 家用电脑](https://hackaday.io/project/19000-a-4-4ics-z80-homemade-computer-on-breadboard)，以及一个很棒的 Hackaday 奖品入口。

那么，他需要什么来建造一台加载了 Forth、CP/M 和 Basic 的逆向计算机呢？CPU 是必需品，而且[Just4Fun]发现了一个 Z80(技术上是 Z84C00 ),价格略高于一美元。一台计算机也需要一些内存，而 128 千字节的并行 SRAM 正好是另一美元的入场券。

事情变得更有趣了。昔日的复古计算机装载的是胶合逻辑、PLA 或其他古怪的芯片，而现代技术已经取得了长足的进步。[Just4Fun]没有使用大量的胶水，而是使用 ATmega32A 进行所有的 I/O、地址解码和串行终端。

扔进这个老式芯片聚宝盆的 ATmega 本身已经有十多年的历史了，但它确实有 40 个引脚和 32 kiB 的闪存。这足以“虚拟化”Z80 总线上需要的所有外围设备，并为计算机的其余部分提供时钟信号。

这台家用电脑最初是在一个无焊试验板上设计和布局的，但是[ [WestfW](https://hackaday.io/westfw) ]设法将这一切都塞进了一个小 PCB。这是一台便宜的电脑，可以让你得到所有逆向计算的好东西，它的随机性足以成为 Hackaday 奖 everything Goes 部分的完美参赛作品。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)