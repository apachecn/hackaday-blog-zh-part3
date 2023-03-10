# 并行端口的 Vaporwave

> 原文：<https://hackaday.com/2018/06/07/vaporwave-for-the-parallel-port/>

调频合成是 80 年代的声音，是商场和麦金塔 Plus 的声音。这是摩托罗拉 DynaTAC 的声音，赫利俄斯半身像，和サ蒸汽波的声音閲ユ.对这种声音最负责的芯片是 OPL2 和 OPL3，由雅马哈生产的芯片上的微型调频合成器，以及 AdLib 和 Sound Blaster 声卡的核心。它是所有伟大的 DOS 游戏中音乐背后的芯片。

不幸的是，计算机不再有 ISA 插槽，卡不能在 486 和基于奔腾的笔记本电脑上工作，这是逆向计算爱好者的最新热点。对于他的 Hackaday 奖参赛作品，[serdef]正在用 OPL2LPT 将 80 年代的声音带到并行端口[。这是一个用于并行端口的声卡，不仅仅是一个像 Covox Speech 那样的电阻 DAC。](https://hackaday.io/project/28665-opl2lpt)

OPL2LPT 的设计非常符合您的预期；这是一个 OPL2 芯片、运算放大器、1/8 英寸插孔和一些无源元件。这里真正的诀窍在于驱动程序；默认情况下，每个 DOS 游戏都希望在端口 338h 上有一个 Adlib 卡，而并行 post 是在 378h 上。驱动程序在软件中处理这个问题，但是可以给游戏打补丁，将每次对 Adlib 卡的写操作改为对并行端口的写操作。

已经，[serdef]的并行端口图形卡是一个真实的，工作的*产品*，已经引起了懒惰的游戏评论和 8 位家伙的注意，你可以看看下面的视频评论。

 [https://www.youtube.com/embed/z3DU2mNBa6M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/z3DU2mNBa6M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/1yB-O4TFIz8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1yB-O4TFIz8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)