# 黑进 Thotcon 0x8 徽章

> 原文：<https://hackaday.com/2017/05/10/hacking-the-thotcon-0x8-badge/>

[Kenjo]上周参加了芝加哥的 Thotcon，并开始黑掉大会徽章并详述他所学到的东西。Thotcon 的徽章由[Jedha]设计，由[88](http://workshop88.com/)车间的[约翰·沃利斯]编程，里面装满了必要的电子硬件和神秘的线索。有四个新像素 led，三个 pots 和一个微型 USB，都由 ATmega32u4 运行。

股票固件是一个名为 tesserHack 的游戏，一个使用三个罐子进行导航的迷宫游戏。也可以通过 USB 连接，通过串口控制台玩，这个版本包括地图视图和帮助菜单。

[Kenjo]之前黑了 Thotcon 0x6 徽章的人，不小心删除了今年徽章上的股票固件，所以他用一个总线盗版商作为 ISP 来烧 Arduino 引导加载程序，并已经开始绘制 pots 和 led。如果你有兴趣帮忙，请登录 Hackaday.io 查看这个项目