# 爬地牢，一次 64 像素

> 原文：<https://hackaday.com/2018/05/05/crawling-a-dungeon-64-pixels-at-a-time/>

视频游戏的趋势是无法将它们与真人电影区分开来，游戏工作室也越来越难与电影工作室区分开来。但是高质量的图形并不总是转化为高质量的游戏性，极简主义的图形可以完成很多事情。让时光倒流几十年，想想《吃豆人》(Pac-Man)、《太空入侵者》(Space Invaders)甚至《乒乓》(Pong)这样的经典游戏，如果你对此有任何怀疑的话。

但即使 Pong 也有超过 64 像素的像素，这就是为什么这个 8×8 RGB 矩阵的地牢爬虫游戏如此吸引人。你可能认为[stoli ist]的游戏会尽可能简单，但再想想。下面的视频展示了它的运行，虽然新用户需要一些帮助来理解各种颜色的含义，但这个游戏非常吸引人。地牢的结构是随机的，有多个关卡可以通过能量箱的内容来解锁，并且在放大的显示中有小怪可以战斗。游戏在 Arduino Uno 上运行，矩阵由一堆 74HC595 移位寄存器驱动。

看到用尽可能少的资源就能完成的事情是很有趣的。寻找更多低分辨率的好？看看这个极简动画展示，或者[一个带矩阵显示的盖革计数器](https://hackaday.com/2015/05/25/led-matrix-plus-geiger-counter/)。

 [https://www.youtube.com/embed/9mStsnL-OEc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/9mStsnL-OEc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

