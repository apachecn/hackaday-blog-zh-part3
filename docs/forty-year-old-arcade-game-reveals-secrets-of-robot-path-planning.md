# 四十岁的街机游戏揭示了机器人路径规划的秘密

> 原文：<https://hackaday.com/2016/04/28/forty-year-old-arcade-game-reveals-secrets-of-robot-path-planning/>

对一个 40 年前的视频游戏进行逆向工程能得到什么？事实证明，非常多，而且你会从[【诺伯特】最近在维也纳聚会](https://www.youtube.com/watch?v=PrPmHPc0vWA)上的讲话中了解到，这不仅仅是让经典重现。

这款游戏名为 [Kee Game 的 Sprint 2](http://www.arcade-history.com/?n=sprint-2&page=detail&id=2596) ，是一款单色的 2D 赛车，允许两名玩家进行面对面的比赛。辉煌的收获金和焦橙配色方案只是尖叫 20 世纪 70 年代，可能很难看出为什么这个游戏曾经是一个受欢迎的四分之一。但当时它很吸引人，[诺伯特]对逆向工程很感兴趣。他做到了，使用 JavaScript 构建了一个忠实的基于浏览器的游戏仿真。他更进一步，创造了这款游戏的 3D 第一人称版本。

但真正的工作开始于拆开占据赛道的计算机控制汽车的人工智能，并理解如何使用每条赛道背后的矢量地图来沿着平滑的路径移动机器人汽车。[Norbert]介绍了矢量场和梯度场的概念以及 Gauss-Seidel 算法，然后将所有这些内容与自主车辆的路径规划联系起来。对于一个承认自己既不是职业程序员也不是数学家的人来说，这是相当令人印象深刻的东西。

我们之前已经报道了大量的街机游戏[港口](http://hackaday.com/2014/04/14/neo-geo-arcade-gets-second-life-with-a-raspberry-pi/)和[娱乐](http://hackaday.com/2012/12/22/fabricating-hardware-from-the-original-arcade-pong-schematics/)，但是这个项目远远不止这些，至少在经验教训方面。

 [https://www.youtube.com/embed/PrPmHPc0vWA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/PrPmHPc0vWA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

