# 便携式 DVD 播放器获得树莓 Pi 零升级

> 原文：<https://hackaday.com/2018/04/13/portable-dvd-player-gets-raspberry-pi-zero-upgrade/>

你可能还记得有一段时间，人们认为便携式 DVD 播放器是一个非常好的主意。在上网本、廉价平板电脑甚至可以说是智能手机被广泛采用之前的日子里，随身携带一台除了播放电影什么也不做的设备似乎是完全合理的。今天，我们回头看它们，就像看翻盖式手机一样:这是我们目前所处的技术过载的一个古怪的前兆。但事实仍然是，数以百万计的这些滑稽的小设备被注入了消费电子市场贪婪的血盆大口。他们已经成熟了，你需要的只是一些灵感。

[![](img/acdbaca34f467c77c4a52561dff98bf3.png)](https://hackaday.com/wp-content/uploads/2018/04/pidvd_detail.jpg) 因此，如果便携式 DVD 播放器和由【nutsacrilege】创造的树莓派 Zero W 的这种嫁接没有让你在当地的二手商店四处寻找捐赠设备，那就没什么可以了。通过集成运行 Kodi 的 Pi，播放器获得了多媒体的支持，可以说弥补了过时的外形。它不仅可以播放各种各样的本地和在线内容，而且如果你愿意，它甚至可以作为便携式游戏系统使用。

放心，这不是什么偷懒的五分钟 mod。所有原始的物理控制都通过连接到 Pi 的 GPIO 的 MCP3008 ADC 和一些聪明的 Python 脚本实现了功能。甚至耳机插孔也通过将其连接到 USB 声卡而变得实用，通过集成一个小型的剥离式集线器，他还可以添加一个外部 USB 端口。当你可以插入一个装满内容的闪存盘时，谁还需要光盘呢？

说到这里，[nut sacrique]报道说，经过他的所有修改，该设备的原始功能仍然完好无损。因此，如果你能让博物馆借给你一个，你甚至可以按照它的创造者的意图在上面播放 DVD。

幸运的话，这个项目将有助于刺激一些更便携式的 DVD 播放器黑客，我们已经看到[珍贵的小至今](https://hackaday.com/2008/02/06/20-mini-dvd-player-lcd-hacking/)。坦率地说，这将是很高兴看到人们[把树莓派的](https://hackaday.com/2016/04/10/gameboy-case-lives-on-with-a-pi-zero/)塞进别的东西[而不是游戏机](https://hackaday.com/2016/11/12/pi-zero-transforms-to-game-boy/)。

[via [/r/raspberry_pi](https://www.reddit.com/r/raspberry_pi/comments/8bmbu5/old_dusty_portable_dvd_player_given_new_life_with/)