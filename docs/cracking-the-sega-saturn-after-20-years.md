# 20 年后破解世嘉土星

> 原文：<https://hackaday.com/2016/07/11/cracking-the-sega-saturn-after-20-years/>

20 年前发布时，世嘉土星是迄今为止最强大的视频游戏机。这是一款革命性的设备，拥有令人难以置信的(在当时)图形，以及世嘉可以借鉴的巨大 IP 库。土星很快被索尼 Playstation 盖过，很快这些设备发现自己没有被使用，没有被喜爱，并在收藏家市场上获得了很高的价格。

在一次去日本的旅行中发现了一个世嘉土星之后，[jhl]决定为这台机器写一些代码。与早期的控制台不同，在早期的控制台中，闪存很容易获得，而在后来的控制台中，直接写入板载存储很容易，为 Saturn 提供一个开发环境并不容易。最好的方法是安装一个 mod 芯片并清除刻录的 CD。与其为土星写一两个游戏，[jhl]分心了几年[并开发了一个光驱模拟器](http://assemblergames.com/l/threads/saturn-optical-drive-emulator.62274/)。

根据[jhl]的说法，世嘉土星的设计极其复杂。有一个完整的芯片专用于控制 CD 驱动器，经过一些严重的逆向工程工作，[jhl]已经很清楚了。接下来的问题是如何将数据装载到土星上。为此。【jhl】[转向土星](http://assemblergames.com/l/threads/saturn-cd-block-rom-dumped.52419/)上的内部扩展端口。这个内部扩展端口被设计成接受 MPEG 解码卡，用于在 Saturn 上播放视频 CD，但是连接器代表整个总线。通过连接一个 Game Boy 闪存盒，[jhl]能够将 ROM 转储到 CD 控制器上。

通过一点点工作，一个快速 ARM 微控制器和一个用于所有逻辑胶水的 CPLD，[jhl]建立了一个适配器，通过这个内部扩展端口将 CD 数据推送到 Saturn。这不仅是自制土星开发的福音，而且这种构建还完全取代了土星中的 CD 驱动器——这是这台 20 岁机器的常见故障点。

这个终极土星裂缝的正式发布还没有出来，但它很快就会到来，允许任何仍然拥有土星的人享受所有这些非常块状的游戏，并开发自己的游戏。你可以在下面查看一个关于[jhl]努力的简短的业余纪录片。

 [https://www.youtube.com/embed/jOyfZex7B3E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jOyfZex7B3E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

