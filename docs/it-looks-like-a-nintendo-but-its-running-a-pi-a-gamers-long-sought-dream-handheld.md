# 它看起来像一个任天堂，但它运行的是 Pi:一个游戏玩家长期寻求的梦想掌上电脑

> 原文：<https://hackaday.com/2018/04/02/it-looks-like-a-nintendo-but-its-running-a-pi-a-gamers-long-sought-dream-handheld/>

[![](img/94cbfcfb4679e50e71725185a7f66931.png)](https://hackaday.com/wp-content/uploads/2018/03/piswitch-internals.jpg) 【克里斯多夫·富特】小时候玩的游戏没有他想玩的多。在使用 RetroPie 和 PiGRRL 2 多年后，当他第一次拿起开关的 joy-cons 时，灵感出现了。看哪:那个[皮开关](https://www.raspberrypi.org/magpi/piswitch-nintendo-switch-console/)！

意识到他们[使用蓝牙技术](https://hackaday.com/2017/11/06/reverse-engineering-the-nintendo-switch-joy-cons/)，【Foote】花了相当多的时间让 joy-cons 正确地与 Raspberry Pi 3 配对，并作为一个控制器运行。一旦完成，他就依靠 Linux 操纵杆映射器来管理键盘绑定，并做一些额外的跑腿工作，以使模拟操纵杆正常工作。

为了让这台游戏机可以移动，他在设备中装入了 6600 毫安时电池和 Adafruit Powerboost 1000c，添加了第二个耳机插孔和扬声器，用于通勤和家庭娱乐，以及 Pi V2 相机模块。一个 3D 打印的外壳，封装了这些组件和一个 7 英寸的触摸屏，也允许 joy-cons 分离——尽管他计划在未来更新其设计。

PiSwitch 启动到一个定制的 UI，让你选择不同的服务——retro pie、Kodi、Debian 和 terminal——而 joy-cons 无缝地一起或单独运行，而不管活动如何。休息之后，请查看该项目的快速介绍之旅！

 [https://www.youtube.com/embed/LGCe-OtNEpA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LGCe-OtNEpA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



他和他的儿子喜欢它，但[Foote]计划在未来增加蒸汽流功能。关于这个版本的更多信息，他的[指令指南](http://www.instructables.com/id/PiSwitch/)已经介绍过了。

[Via [/r/raspberry_pi](https://www.reddit.com/r/raspberry_pi/comments/88az74/piswitch_build_your_own_nintendo_switch_console/)