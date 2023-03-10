# PIC16Maze 迷宫升级秘密迷宫游戏

> 原文：<https://hackaday.com/2018/05/09/pic16maze-upgrades-secret-maze-game/>

我们真的很喜欢读者从他们在 Hackaday 上看到的东西中受到启发，在此基础上进行构建，并让我们知道，这样我们就可以将它传递下去。在这种情况下，[Vegipete]用最少的部件和一些巧妙的软件技巧制作了一个秘密迷宫游戏。

它围绕 8 引脚 PIC16F18313 微控制器构建，使用操纵杆进行输入，使用 9 个 WS2812 LEDs 显示玩家和周围的迷宫墙。他的灵感来自[戴维·约翰逊-戴维斯的] [极简主义的秘密迷宫游戏](https://hackaday.com/2018/02/04/a-game-that-does-more-with-less/)围绕着 8 针 ATTiny85 打造。在那一个中，[David]巧妙地使用了 charlieplexing 来获得四个引脚来控制四个 led 和四个按钮。[vegi Pete]使用 WS2812 LEDs 允许他仅用一个引脚来控制 led，并且还可以在使用三个引脚来控制操纵杆及其按钮时获得颜色。他将来可能会用另一个针来发声和振动。

他详细介绍了 WS2812 协议，即如何使用一个引脚和不同的脉冲长度来表示 0 和 1，从而与 led 进行通信。我们将让您看到他的帖子以获得更多深度，但基本上，他在 PIC 上引入了一个名为可配置逻辑单元(CLC)的模块，使这一点变得简单，并释放处理器周期以供用户代码做其他事情。

他的源代码可以应要求获得，但他确实详细说明了他用来旋转视图的一个巧妙的软件技巧。这可能会让一些人感到困惑，但当你在迷宫中移动时，你的视点会旋转，因此向上总是你面对的方向。幸运的是，用户周围的墙可以用 8 位来表示，东、西、南、北各 4 位，另外 4 位表示角落。迷宫被存储为位图，并从中提取当前位置的 8 位值，每一位代表该位置周围的一堵墙。要旋转墙壁以匹配用户的当前方向，只需根据需要移动位即可。然后将它们移出以设置每个 LED。看看下面的视频吧。

尽管接口和器件数量很少，但它工作得非常好。

 [https://www.youtube.com/embed/7q9Lj8uryXg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/7q9Lj8uryXg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

