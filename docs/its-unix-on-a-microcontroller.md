# 是 UNIX。在微控制器上。

> 原文：<https://hackaday.com/2018/06/03/its-unix-on-a-microcontroller/>

在一个类似 UNIX 的操作系统放在你口袋里的时代，很难表达曾经有一段时间，仅仅一个词就足以传达巨大计算能力的光环。如果你运行 UNIX，你的电脑可能会占满一个房间，你会用它来处理重要的事情，而不仅仅是查看你的 Twitter feed。UNIX 机器可能仍在执行高端任务，但摩尔定律在这中间的几年里兑现了它的承诺，你的装有类似 UNIX 操作系统的手机比 20 世纪 70 年代那种房间大小的小型机功能强大得多。一个几美分的芯片就能完成这项工作，这就引出了一个问题:今天我们运行 UNIX 需要多少的芯片？这是[Joerg Wolfram]可以给你的建议，因为他有一个运行在微控制器上的功能 UNIX。

当然，无论是在 20 世纪 70 年代还是现在，这里讨论的 UNIX 都与你在超级计算机上看到的不完全相同。Mini UNIX 是 40 年前由贝尔实验室的 Heinz Lycklama 开发的操作系统的极简版本。它为 DEC PDP-11 提供了一个完整的 UNIX V6 系统，但只需要 56K 的 RAM，没有 MMU。在 STM32 微控制器上仿真 PDP-11 可以让它愉快地运行，虽然它不是最简约的微控制器，但它仍然是运行 UNIX 的一个非常便宜的部件。

在商用微控制器上运行的 20 世纪 70 年代版本的操作系统是否会风靡全球还值得怀疑，但这并不是如此简洁的黑客攻击的目的。这当然不是我们第一次看到类似的工作，尽管这个 PIC32 提供的资源要多一点。

标题图片:Golonlutoj [ [CC BY-SA 3.0](https://commons.wikimedia.org/wiki/File:MicroSTM32.jpg) 。