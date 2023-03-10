# 把汽车变成游戏控制器

> 原文：<https://hackaday.com/2017/12/22/turn-a-car-into-a-game-controller/>

自 20 世纪 80 年代末推出以来，CAN 总线已成为汽车工程的主要组成部分，但与此同时，随着电子设备的普及，汽车内的几乎每一件设备都被放到了 CAN 总线上。虽然人们对这是否是一件好事有不同的看法，但现实是，总线上已经收集了足够的数据，只需一点点代码就可以将一辆未经改装的现代汽车变成一个视频游戏控制器。

[斯科特]项目的核心是一台笔记本电脑和一个 Python 程序，该程序从汽车的 CAN 总线上收集汽车信息，包括踏板和方向盘的位置。通过将适配器插入 OBD-II 端口(1995 年后制造的所有汽车的标准)可以访问这些信息。从那里，笔记本电脑将 CAN 数据解析成键盘和鼠标命令，供您选择视频游戏。

这是对 [CAN 总线](https://en.wikipedia.org/wiki/CAN_bus)本质的一次有趣的调查，但也是对从汽车上获得的所有数据的一次不太危险的演示，比[我们见过的其他一些案例](https://hackaday.com/2015/08/22/how-those-hacker-took-complete-control-of-that-jeep/)要危险。至少[Scott]的马自达(大概)没有任何无线攻击媒介！

 [https://www.youtube.com/embed/MXvI5MorsO4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MXvI5MorsO4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

