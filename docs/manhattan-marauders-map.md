# 曼哈顿活点地图

> 原文：<https://hackaday.com/2017/04/19/manhattan-marauders-map/>

如果你郑重发誓你不怀好意，而你恰好在曼哈顿度过了 95 度以下的大部分时间，那么你会欣赏[这个基于树莓派的曼哈顿掠夺者地图](http://imgur.com/a/AA20C)。

不是说哈利波特主题的地图一定是[GawkyFuse]在创建这个有趣的建筑时的意图；只是曼哈顿的旧貌换新颜——它展示了东河的福利岛，该岛于 1971 年更名为罗斯福岛——给这座建筑增添了一种复古的感觉。这张地图印在普通纸上，覆盖了一个 64×32 LED 矩阵，由 Pi 3 顶上的矩阵帽驱动。

[GawkyFuse]在他和妻子的 iPhone 上使用 OwnTracks 应用程序向 CloudMQTT 报告他们的位置。Pi 向代理订阅，当他们在城市中移动时，用红色更新他的位置，用蓝色更新她的位置；当他们在一起时，一个浪漫的接触是显示一个单独的紫色点。没有任何文字说明当任何一方离开地图区域时会显示什么，但 2048 像素的显示屏提供了很多可能性。

我们以前在这些地方看到过[一个韦斯莱时钟](https://hackaday.com/2013/02/11/harry-potter-location-clock-spies-on-your-smart-phone/)或者[两个](https://hackaday.com/2012/07/30/magic-clock-locates-your-friends/)，但是奇怪的是没有像这样的活点地图。虽然[这张奥地利电车轨道图](https://hackaday.com/2014/09/15/leds-turn-this-paper-map-into-a-tram-tracker/)非常接近【GawkyFuse】的精美设计。

[via [r/raspberry_pi](https://www.reddit.com/r/raspberry_pi/comments/65d6bs/map_that_displays_location_with_led_matrix/)