# 晃动的神奇球探测到稀有的神奇宝贝

> 原文：<https://hackaday.com/2016/08/12/wiggling-pokeball-detects-rare-pokemon/>

[TJ Hunter]希望在盯着屏幕的情况下，在不耗尽智能手机电池的情况下找到一些更稀有的神奇宝贝。他制作的直径 25 厘米的小精灵球可以探测附近的神奇宝贝，如果看到罕见的猎物，它就会摆动提醒主人。

在看起来真实的红白相间的聚苯乙烯泡沫球内部，有一个粒子电子和一个粒子资产追踪器板，这给了它必要的 GPS 和 2G/3G 连接。一个钢筋混凝土伺服与一点重量照顾摇动运动。每一分钟，球都会将其当前的 GPS 坐标发送到[TJ 的]服务器端 Laravel 应用程序，然后该应用程序连接到 Niantic 的服务器(使用[这个库](https://github.com/Armax/Pokemon-GO-node-api))以获得附近神奇宝贝的列表。如果列表中包含一些更罕见的，一个“摆动”命令被发送回球。然后球兴奋地扭动，通知携带者是时候拔出网枪了。仅仅通过挖掘这个球的代码库，你就能保证抓到一个 [Porygon](http://bulbapedia.bulbagarden.net/wiki/Porygon_(Pok%C3%A9mon)) ，一个只由源代码组成的罕见家伙。

 [![Inside of the sphere sits a Particle Electron, tracker and servo](img/af0bf772d2c3f1b9a6f96b857301b31d.png "2016-07-30 12.47.11")](https://hackaday.com/2016/08/12/wiggling-pokeball-detects-rare-pokemon/2016-07-30-12-47-11/) Inside of the sphere sits a Particle Electron, tracker and servo [![Acrylic paint turns the styrofoam into a Pokéball](img/3f509a7c1058d3a8c9cd39a9a97ce0f4.png "2016-07-28 21.46.49")](https://hackaday.com/2016/08/12/wiggling-pokeball-detects-rare-pokemon/2016-07-28-21-46-49/) Acrylic paint turns the styrofoam into a Pokéball [![A rare Porygon has appeared! (wiggle)](img/744d698a1d7d00ae1bdb5751bc8cddc2.png "13090693_661935977304799_369005648_o")](https://hackaday.com/2016/08/12/wiggling-pokeball-detects-rare-pokemon/13090693_661935977304799_369005648_o/) A rare Porygon has appeared! (wiggle)

有一段时间，球坐不住了，因为 Niantic 屏蔽了所有第三方应用。看起来现在天气已经放晴了。pokemongodev 团队结束了为期 4 天的黑客马拉松，[宣布他们已经发现了“未知 6”包](https://www.reddit.com/live/xdkgkncepvcq)中的内容，这是 Niantic 阻止机器人进入游戏的秘密酱料。[TJ]已经让他的球回到线上，我们假设很快一切都会回到*正常*。请欣赏下面的视频，其中[TJ]展示了他的体型:

 [https://www.youtube.com/embed/PeRdUCwL3-Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/PeRdUCwL3-Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

