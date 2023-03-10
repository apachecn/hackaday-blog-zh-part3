# 144 字节的字符生成

> 原文：<https://hackaday.com/2016/12/15/character-generation-in-144-bytes/>

[Jaromir Sukuba]有一个很棒的[BrainF * CK 解释器项目正在进行中](https://hackaday.io/project/18445-brainfcktor)。他用不到 1 kB 的代码处理了整个语言。听起来像是参加 [1 kB 挑战](https://hackaday.io/submissions/the-1kb-challenge/list)的好机会。唯一的问题是用户界面。最初的设计使用了 4 行字符的液晶显示器。这些 LCD 中的 HD44780 控制器有自己的字符表 ROM，仅占用的空间就超过 1 kB。

[Jaromir]可以在没有 LCD 的情况下提交 BrainF*ck 解释器，并且很可能在比赛中取得好成绩。但这对他来说还不够。他知道他可以得到符合比赛规则的基于角色的输出。解决方案是一点创造性的压缩。

Jaromir 创造了一个由 16 个常用模式的单字节向量组成的调色板，而不是一个一个像素的字符表示。字符是由这些矢量组合而成的。每个字符是 4 x 8 像素，所以每个字符使用 4 个向量。困难的部分是为向量选择常用的位模式。

第一次迭代相当有希望——文本通常是可读的，但有几个字符相当糟糕。[Jaromir]坚持下去，减少和优化他的向量托盘两次以上。最终的设计相当不错。每个字符使用 16 位存储空间(四个 4 位向量查找值)。向量托盘本身使用 16 个字节。这意味着 64 个字符只占用 144 字节的闪存。这正是我们希望在 1 kB 挑战赛中看到的黑客攻击。一点创造性的思考能找到绕过看似不可能的障碍的方法。最棒的是[Jaromir]记录了他的工作，所以现在任何人都可以在 1 kB 挑战赛中使用它。

![1kb-thumb](img/c25ee8590ee29cc76bd2ada5afb927dd.png)

如果你心中有一个很酷的项目，还有足够的时间[参加 1 kB 挑战](https://hackaday.io/contest/18215-the-1kb-challenge)！截止日期是 1 月 5 日，所以检查一下，发动你的装配工吧！