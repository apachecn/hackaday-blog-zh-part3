# 象棋人工智能，老派

> 原文：<https://hackaday.com/2017/04/03/chess-ai-old-school/>

在象棋电脑出现之前，人们就对象棋电脑感兴趣了。在 1950 年的一篇论文中，[克劳德·香农]定义了两种主要的下棋策略。显然，实际的国际象棋程序仍然使用他概述的技术。如果你想知道如何让计算机下棋,[FreeCodeCamp]有一个有趣的帖子，带你一步一步地完成[构建象棋引擎](https://medium.freecodecamp.com/simple-chess-ai-step-by-step-1d55a9266977)。

代码是用 JavaScript 写的，但这种方法让我们觉得很老派。然而，当你从随机移动到稍微聪明的策略，再到更深入的搜索时，观察代码的演变是很有趣的。因为它是用 JavaScript 编写的，所以你可以在你的浏览器中跟随它，发现程序何时变得足够聪明来击败你。最终版本甚至在 [GitHub](https://github.com/lhartikk/simple-chess-ai) 上。

这个算法很经典。首先，对于每一个棋子，你要评估可能的走法并给它们打分。然后你生成所有可能的对手动作，并对它们进行评分。你继续尽可能地深入，但是搜索空间很快变得很大。为了使思考更简单，考虑一个 4×4 的棋盘，一边有四个红色的方格，另一边有四个黑色的方格。对于第一步，有四个可能的步骤。那么这四个答案中的每一个都有四个可能的答案，总共是 20 (4 + 16)。随着跳棋被捕获或阻塞，情况会变得更糟。而那只是一块很小的板子，上面的棋子不太能动。彻底搜索这些移动是非常昂贵的。

不过，假设你有棋步，算法会假设你的棋步会提高其位置的等级，而对手会以最小化等级的方式移动。此外，某些试探法和其他算法会提前终止搜索，让计算机在给定的时间内更深入地评估有希望的移动。

当然，这只适用于你对某个特定职位的“好”或“坏”程度的试探。如果你跟随这篇文章，你将有一个框架，在那里你可以尝试你自己的想法。我们之前已经看过一些硬件棋手，包括那些使用 T2 标准接口的棋手。当然，最新的热潮是国际象棋的[深度学习](https://hackaday.com/2015/10/02/computer-learns-to-hack-chess/)，但是仍然有很多程序使用旧的学校技术。如果你想知道更多，请看下面来自[帕特里克·温斯顿]的麻省理工学院的视频。

 [https://www.youtube.com/embed/STjW3eH0Cik?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/STjW3eH0Cik?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

