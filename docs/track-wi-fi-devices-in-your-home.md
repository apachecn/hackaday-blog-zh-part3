# 跟踪家中的 Wi-Fi 设备

> 原文：<https://hackaday.com/2016/12/25/track-wi-fi-devices-in-your-home/>

你如何审计你家的 Wi-Fi 网络？也许你登录到你的路由器，看看连接的设备。有时你会发现一个意想不到的客人，但一点点的侦查工作通常会把你带到小侄子的游戏控制台或你长凳上被遗忘的 ESP8266。

如果你的路由器能告诉你*所有连接到它的设备在哪里*难道不是很有用吗？如果你是[Zack Scholl]，你可以做所有这些甚至更多，因为他的 [FIND-LF 系统记录其范围内所有 Wi-Fi 设备的 Wi-Fi 探测请求](https://github.com/schollz/find-lf)，即使它们没有连接，并根据它们在几个嗅探接收器上的相对信号强度三角测量它们的位置。这些接收器是一个带有自己的 FIND-LF 服务器的 Raspberry Pis 网络，它们收到的任何探测请求都被转发到[扎克]的[FIND server](https://github.com/schollz/find)(他的另一个项目)，后者负责整理设备的位置。

这是一件令人印象深刻的作品，尽管每个接收器都有一个树莓派，可能会有点贵。除了这里提到的两个项目，Zack 还在这个领域做了其他工作，他的其他工作包括[*哈利波特*活点地图的实现。

这绝不是这些年来我们见过的唯一的室内定位系统。[比如使用 ESP8266 模块](http://hackaday.com/2015/05/07/hackaday-prize-entry-subterranean-positioning-system-subpos/)的，或者[这种商业产品](http://hackaday.com/2015/06/17/new-part-day-indoor-location-systems/)类似于这里显示的项目。