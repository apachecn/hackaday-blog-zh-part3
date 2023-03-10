# 字钟的自动化设计

> 原文：<https://hackaday.com/2018/04/17/automating-the-design-of-word-clocks/>

单词钟，或者一个发光字母矩阵，拼出时间，是所有有进取心的电子爱好者的标准配置。问题是找到正确的方法来驱动 led 矩阵，并投入大量脑力来创建一个字母矩阵，它将拼写出时间，而不会让它看起来像是应该拼写出时间。

为了今年的 Hackaday 奖参赛作品，[Stephen Legge]正在创建一个标准工具包，使单词时钟更容易构建。这是一个硬件和软件项目，允许任何合理大小的 LED 矩阵，软件可以制作一个字母网格，只拼出你想要的单词，而不是你不想要的四个字母。

这个项目的硬件是围绕 ISSI 的 IS31FL3733 LED 驱动器构建的。这是一个有趣的芯片，它接受了 I2C，并吐出了一个 LED 矩阵，只有很少的额外支持组件。这个芯片为[Stephen]提供了 12×16 的单色 LED 矩阵，对于一个字时钟来说绰绰有余。

这个构建变得稍微有趣一点的地方是创建了一个自定义的字母矩阵，当以适当的方式照亮时，它仍然会拼出“15 分钟到中午”。这是创建定制单词时钟的一大挑战；你总是可以从另一个单词时钟中借用字母的布局，但是如果你想要定制短语，你要么必须坐下来用铅笔和绘图纸，要么编写一些软件来自动完成。

这是一个伟大的项目，因为[Stephen]的所有工作都是在开源许可下发布的，所以这是进入 Hackaday 奖第一部分的一个很好的机会，在这个部分中，我们挑战硬件创造者来构建开放硬件。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)