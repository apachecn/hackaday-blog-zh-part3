# Hackaday 奖参赛作品:微型矩阵 Charlieplexed 显示器

> 原文：<https://hackaday.com/2017/04/04/hackaday-prize-entry-micro-matrix-charlieplexed-displays/>

如果您需要一款超薄、低功耗的显示器，并且不需要在微控制器上使用一大堆引脚，[bobricius]正是您所需要的。他今年的 Hackaday 奖参赛作品是一个 Charlieplexed LED 显示屏。借助该板，您可以仅使用 11 个 GPIO 引脚来驱动 110 个 led。

Charlieplexing 在这些地方有点黑暗。这并不是说这个理论很难；它实际上只是从 GPIO 引脚流出或吸收电流，并将 led 排列成彼此不平行。理论是一回事，实施是另一回事。要构建一个 Charlieplexed LED 矩阵，你需要对 PCB 布局有点疯狂，如果你在 perf 板上进行点对点布局，上帝会帮助你的。

不知何故，[bobricius]设法在一个 PCB 上安装了 110 个 led，同时设法将这些信号线连接到电路板一侧的一组合理的焊盘上。驱动所有这些 led 只需要 11 个引脚，这使得该项目成为一些非常酷的可穿戴设备或其他需要明亮、低分辨率显示器的项目的良好基础。

由于[bobricius]可以在一块小板上放置 110 个 led，他显然可以从那块板上拿走 led。这就是他在设计成时钟的精简版[中所做的。两者都是很棒的小电路板，是低引脚数的微型显示器的完美解决方案。](https://hackaday.io/project/18014/log/48764-very-reduced-number-only-version)

 [https://www.youtube.com/embed/n3ySo1sJKf4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/n3ySo1sJKf4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)