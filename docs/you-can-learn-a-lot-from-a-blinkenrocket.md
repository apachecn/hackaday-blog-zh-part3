# 你可以从 Blinkenrocket 中学到很多

> 原文：<https://hackaday.com/2018/02/02/you-can-learn-a-lot-from-a-blinkenrocket/>

在今年的混沌通信大会上，我们采访了[muzy]和[overflo],他们带着徽章和焊接项目出席了会议，他们旨在教年轻人如何焊接和编程。Blinkenrocket 基本上是一个 64 LED 矩阵显示器，仅够存储和显示动画的支持硬件，从我们在与会者脖子上看到的闪烁的火箭数量来看，这是一个成功。

他们在 34C3 的谈话主要涉及生产细节、设计改进以及生产数千件产品的缺陷。如果你正在考虑建立这样规模的硬件套件或徽章，你真的应该去看看，并抄袭他们的一些生产优化技巧。

例如，他们没有给零件贴上“C2”或“R: 220 欧姆”的标签，而是使用了一种简单的颜色编码方案。这不仅让孩子们更容易组装，也意味着他们不必在每个部件上都贴上 1000 个零件标签。再加上[overflo]的 [Zerhacker](https://hackaday.com/2017/10/06/tape-cutting-bot-trims-the-tedium/) ，条状的 SMD 零件被切割成合适的长度，并通过机器一步完成颜色编码。

Blinkenrocket 本身最酷的功能就是音频编程界面。这就像在过去糟糕的日子里，软件存储在磁带上一样，但这是一个非凡的界面，可以从网络应用程序中获得简单的动画，并直接进入一个最小的硬件——只需将其插入笔记本电脑或手机的音频输出，然后在浏览器中按下“播放”。最初的设计试图将数据编码为方波的脉冲长度，但这被证明是非常依赖于硬件的。最终的设计采用了频移键控。旧的又是新的。

你想知道的关于设计、代码甚至网站本身的一切都在[项目的 GitHub 页面](https://github.com/blinkenrocket)上，所以去看看吧。如果你想自己安排一个 Blinkenrocket 工作室，可以发一封电子邮件。充分披露:[overflo]给了我们一个套件，带有 ~~0805~~ 1206 部件的“硬模式”SMD，组装和编程很有趣。

 [![Before...](img/f35831fcc75ab686cc97edffff7368bc.png "DSCF0448_thumbnail")](https://hackaday.com/dscf0448_thumbnail/) Before… [![After](img/c8a20220b5f0b20fb7150e8821c65eae.png "DSCF0451_thumbnail")](https://hackaday.com/dscf0451_thumbnail-2/) After