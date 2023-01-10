# 细胞自动机浏览器

> 原文：<https://hackaday.com/2016/09/30/cellular-automata-explorer/>

我们都知道康威的生命游戏中的细胞自动机，它使用基于所有八个相邻细胞状态的规则来模拟细胞进化。[Gavin]在业余时间一直在玩基本的细胞自动机。与康威的游戏不同，初等自动机只使用一个单元的左右邻居来确定该行前面的下一个单元。尽管相对简单，一些真正复杂的模式出现了，包括一个图灵完全模式。

[Gavin]开始用手做计算是为了好玩。他为此制作了一些漂亮的工作表。正如我们很容易想象的那样，手工计算很快就变得令人厌烦。没过多久，他的想法就转向了自动化他的细胞自动机。所以，他组装了一个自动细胞自动机。(我们承认，我们觉得这有点好玩。)

这可能是一个快速的软件项目，但一半的乐趣是在一个专门构建的生态系统上看到模拟。构建设备的文件[存放在 Thingiverse](http://www.thingiverse.com/thing:1788244) 上。像[其他细胞自动机项目](http://hackaday.com/2014/01/11/extremely-slick-game-of-life-based-clock/)一样，它使用 LED 矩阵来显示数据。一个 Arduino 充当大脑，一些来自世界上最[组织荒谬的电子产品收藏](https://www.youtube.com/watch?v=x8nbHYOc8ns)的非常酷的复古开关完成了这个项目的外观。

要使用，输入底部开关的起始条件。Arduino 上的代码然后计算并在矩阵上显示图案。非常酷，而且比手工操作要快得多。