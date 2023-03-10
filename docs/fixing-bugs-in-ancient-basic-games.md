# 修复古代基础游戏中的 bug

> 原文：<https://hackaday.com/2017/07/05/fixing-bugs-in-ancient-basic-games/>

在大家都在栈交换上学习编程之前，事情就大不一样了。电脑杂志里有基本的程序，读者可以一行一行地打出来，然后点击运行。从理论上讲，这是一种很糟糕的学习编程的方式；这只是简单的死记硬背，而没有深入了解代码实际在做什么。当然，从 Stack Exchange 复制和粘贴是完全一样的事情，所以也许这些杂志走在了曲线的前面。

[0xA000]最近偶然发现他的一本旧电脑杂志，里面有*的输入列表，这是一款让你在迷宫中盲目漫步的游戏。当[0xA000]在 1988 年将这个游戏输入他的 C64 时，这个游戏无法运行。三十年后，他决定再试一次，结果[修复了一个旧电脑游戏](http://0xa000.blogspot.nl/2017/06/fixing-bugs-like-its-1988.html)的漏洞。*

 *当[0xA000]在 1988 年将这个游戏输入他的电脑时，地图就是不起作用，最终的屏幕显示出一个迷宫，墙壁在它们不应该在的地方。快速搜索一下谷歌，就能找到有同样问题的同一款游戏的磁盘映像。这个 bug 很明显是在游戏结束时绘制地图的代码部分，所以[0xA000]开始在那里寻找。代码中令人不快的错别字是$F4 而不是$F5，或者是 244 而不是 255。这使得地图的颜色移动了 11 个位置，这意味着在最终屏幕上标记为已访问的位置是错误的。这个错误是在开发过程中突然出现的，还是仅仅是杂志排版时的一个简单的打字错误，现在已经不重要了；29 年后，这个 bug 修复了。*