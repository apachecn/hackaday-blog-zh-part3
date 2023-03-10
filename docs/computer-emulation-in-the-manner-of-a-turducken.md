# 以火鸭鸡的方式进行的计算机仿真

> 原文：<https://hackaday.com/2016/11/02/computer-emulation-in-the-manner-of-a-turducken/>

如果你来自一个有吃烤火鸡或烤鹅来庆祝圣诞节、感恩节或其他节日的传统的地方，那么你可能会遇到三鸟烤肉或火鸭。一只去骨的鸭子和一只去骨的鸡一起被塞进火鸡里，所有的空隙都被香肠肉馅填满，最后的混合物被烤成一顿丰盛的烤肉大餐。素食者，请把目光移开。

这是一种过多的家禽，但三鸟烧烤是一种美味，绝对有效。我们不太确定是什么联系让我们想起了火鸭鸡，从而让我们开始了庆祝家禽菜肴的旅程，但我们会把结论留给读者。有人创造了一个邪恶的火鸭式模拟器链，通过 Windows、DOS 和 Commodore 64 在 Linux 机器上提供辛克莱 ZX 频谱。如果它像家禽菜一样有自己的词，它可能是 Linwindoscomtrum，但我们不要去那里。

[![The linwincomtrum in all its glory.](img/a8d6caed5f0af306e04997ee3a03c22e.png)](https://hackaday.com/wp-content/uploads/2016/11/spectrum-screengrab.png)

The linwindoscomtrum in all its glory.

那么他们是如何做到的呢？首先，他们拿了[鲁本图](http://lubuntu.net/)，装了[酒](https://www.winehq.org/)。(好吧，WINE 不是一个模拟器，我们知道这一点，但先不要急着讲这个故事)然后他们在 Wine 下安装了 [DOSBox](http://www.dosbox.com/) 作为 DOS 命令提示符，并运行了 [no$C64](http://problemkaputt.de/c64.htm) ，一个 Commodore 64 模拟器。在那上面，他们运行了辛克莱·ZX 频谱模拟器，最后到达了 ZX BASIC 提示符。

作者在文章开始时确实指出了这是十分钟的浪费，但即使结果是在现代电脑上缓慢地模拟一台古老的家用电脑是一种过于复杂的方法，我们仍然会给他们的努力打十分。

顺便说一句，作者没有表明自己的身份，网站的其他部分也没有什么线索可以表明他们的身份，所以对于一篇黑客文章来说，我们不能给予应有的赞扬，这是不寻常的。然而，我们向匿名的模拟器飞行员致敬，他们光荣的愚蠢。

如果 ZX 激起了你的兴趣，我们已经为过去的橡胶键英国微型电脑制作了编码教程，以及后来的磁带驱动器切除教程，当然还有业余无线电爱好者的业余无线电接收器。

Via [黑客新闻](https://news.ycombinator.com/item?id=12842868)。ZX 频谱图像:比尔·伯特伦[CC BY-SA 2.5]，通过[维基共享资源](https://commons.wikimedia.org/wiki/File:ZXSpectrum48k.jpg)。