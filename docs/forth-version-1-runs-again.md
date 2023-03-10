# 第四个版本 1 再次运行

> 原文：<https://hackaday.com/2018/03/27/forth-version-1-runs-again/>

有些人喜欢爱情，有些人讨厌爱情。然而，你通常认为 Forth 是运行在小型计算机上的东西，比如 8 位微型计算机。当(查克·摩尔)在 20 世纪 60 年代开发该系统时，它运行在 IBM 1130 上。[Carl Claunch]扫描了一份原始代码清单，[让它再次运行](https://rescue1130.blogspot.com/2018/03/historical-recreationrestoration-of.html)。

实际上有几篇详细的博文。幸运的是，Forth 非常简单——尤其是核心部分。然而，它与现代的福斯有很多不同之处。最明显的是 dot 关键字开始一个定义，不打印栈顶。然而，内部细节也有所不同——例如，该系统将字符存储在打包的 EBCDIC 中 IBM 计算机使用的一种类似 ASCII 的代码。

奇怪的是，虽然这个项目最终没有成功，但[摩尔]还是用 Forth 编写代码，让大型计算机帮助设计地毯。然而，这种从[摩尔的]私人卡片库发展而来的语言，比机器首选的 FORTRAN 语言更容易使用。

致力于此的小组已经发布了原始扫描，并承诺很快会有机器可读的版本。没有运行它的 IBM 1130 吗？[当然可以](http://ibm1130.org/)。

如果你想要更现代、更小的东西，你可以选择 Hackaday 批准的项目。例如， [Mecrisp-Stellaris 在一只手臂上向前](https://hackaday.com/2017/04/19/moving-forth-with-mecrisp-stellaris-and-embello/)。或者，使用云，然后[在你的浏览器](https://hackaday.com/2017/01/04/browsing-forth/)中运行它。