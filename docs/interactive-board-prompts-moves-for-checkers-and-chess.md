# 交互式棋盘提示跳棋和国际象棋的移动

> 原文：<https://hackaday.com/2017/04/16/interactive-board-prompts-moves-for-checkers-and-chess/>

就设备而言，国际象棋和跳棋是简单的游戏——只有一把棋子和一个棋盘。然而，这种简单性掩盖了游戏潜在的复杂性，并在很大程度上解释了它们数千年来的流行。

用[增加国际象棋和跳棋的交互游戏板](http://www.bogdanberg.com/2017/04/08/smart-game-board-checkers-chess/)的复杂性可能看起来违反直觉。但[波格丹一世·伯格]的项目不仅旨在教授跳棋和国际象棋，还旨在让游戏变得更刺激、更吸引人。看起来有点像桌面版的[互动舞池](http://hackaday.com/2017/03/24/daunting-interactive-led-dancefloor-build-is-huge-win/)，我们最近已经看到了很多，板子是由激光切割的丙烯酸树脂制成的，用胶合板隔断来隔离所有 64 个正方形。新像素和霍尔效应传感器安装在定制的印刷电路板上，可以延伸一行的长度，并连接到具有大量 IO 的 Arduino Mega。游戏棋子是五颜六色的冰箱贴。[波格丹一世]目前的程序支持跳棋，跟踪棋子相对于起始位置移动到了哪里，并提示用户可能的合法移动。

在下面的视频中,[波格丹一世]的板子看起来很有趣，我们喜欢它的质量和不引人注目的交互性。不过，当他开始实施国际象棋时，他可能会想要比冰箱磁铁更好的东西作为棋子。

 [https://www.youtube.com/embed/dvaJOHARcIw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/dvaJOHARcIw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

