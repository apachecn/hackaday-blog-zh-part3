# 位碰撞 VGA 适合在 1 KB 以下

> 原文：<https://hackaday.com/2016/12/08/bitbanging-vga-fits-in-under-1-kb/>

不要把那些老旧的 VGA 显示器扔掉，把它们变成有【danjovic】和 [VGA 闪烁灯](https://hackaday.io/project/8537-vga-blinking-lights)的艺术品。本电路使用 PIC16F688 产生 VGA 视频。也不仅仅是单色点的随机喷射。VGA 闪烁灯可以显示 48 个不断变化的彩色方块。

VGA 闪烁灯最初是为平方英寸比赛设计的，可以藏在硬币后面。[Danjovic]重拾他的项目，并参加了 [1 kB 挑战](https://hackaday.io/contest/18215-the-1kb-challenge)。代码是用 PIC 汇编写的。用于生成平方时钟的最后一个十六进制数为 471 个字。因为 PIC 使用一个 14 位的字，所以刚好超过 824 字节。有足够的空间进行功能扩展！

视频是在 R2R DAC 上扭转产生的。[Danjovic]稍微调整了电阻值，以获得 VGA 标准的正确电压水平。正方形本身的颜色是随机的，使用伽罗瓦线性反馈移位寄存器(LFSR)生成。

由于只有少数几个组件，BOM 成本低于 5 美元，这将是任何硬件黑客的一个有趣的晚上项目。

![1kb-thumb](img/c25ee8590ee29cc76bd2ada5afb927dd.png)

如果你心中有一个很酷的项目，还有足够的时间[参加 1 kB 挑战](https://hackaday.io/contest/18215-the-1kb-challenge)！截止日期是 1 月 5 日，所以检查一下，发动你的装配工吧！

![1kb-thumb](img/c25ee8590ee29cc76bd2ada5afb927dd.png)

如果你心中有一个很酷的项目，还有足够的时间[参加 1 kB 挑战](https://hackaday.io/contest/18215-the-1kb-challenge)！截止日期是 1 月 5 日，所以检查一下，发动你的装配工吧！