# 机器人 808 鼓机

> 原文：<https://hackaday.com/2016/09/18/a-robotic-808-drum-machine/>

如果你在上世纪 80 年代在当地的唱片店闲逛，并且你没有对氨纶和蓬松的摇滚发型的渴望，那么你的收藏中可能会有不止几首那个时期的电子音乐。在那个时代，电子乐器的普及是通过相对便宜的大众市场数字复音乐器的出现实现的，它挤掉了单音模拟合成器的声音，让下一代在接下来的十年里重新发现。单个乐器型号成为图标，并进入了当时的音乐术语，如 Ensoniq Mirage 采样合成器、雅马哈 DX7 FM 合成器或 Roland TR-808 鼓机。

正是罗兰 TR-808 启发了今天的主题，来自[莫里茨·西蒙·艾斯特]的 [MR-808 机器人鼓机](https://hackaday.io/project/14866-mr-808-interactive)。一个打击乐器音序器，所有真实的乐器都内置在一个类似巨大的罗兰 808 的橱柜中。[最初是作为一种表演乐器](http://hackaday.com/2012/11/05/mr-808-is-a-mechanical-version-of-the-most-famous-drum-machine/)建造的，但后来被改造成一件装置艺术品，游客可以为自己编程。

[![Block diagram of the MR-808](img/66f1355eb99612f5b5b2ac374e61a437.png)](https://hackaday.com/wp-content/uploads/2016/09/mr-808-block-diagram.jpg)

Block diagram of the MR-808

在创造者的网站上有[对该机器的设计和建造的全面描述](http://learning.sonicrobots.com/mr-808-technique/)，以及[更高层次的介绍](http://sonicrobots.com/Project/mr-808-interactive/)。为了创造尽可能接近罗兰声音的机械乐器，投入了大量的努力，每个乐器都由 MIDI 控制的 Arduino Mega 驱动的螺线管操作。第二个 Arduino，这次是一个 Uno，控制着跟随乐器的灯光。

装置的[交互部分](http://learning.sonicrobots.com/2016/05/20/kiosk-mode-for-nexus-7-tablets-for-an-interactive-installation/)来自 Nexus 7 平板电脑上网络浏览器中运行的音序器前端，这似乎是由为 MR-808 提供 MIDI 的 Raspberry Pi 提供的。

结果可以在休息时间下面的视频中看到，从观众的反应来看，这台机器相当受欢迎。

 [https://www.youtube.com/embed/RU2BB7RFBLM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/RU2BB7RFBLM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们在 Hackaday 展示了不少经典的罗兰合成器。一辆真正的罗兰 808 [收到了一个 MIDI 接口](http://hackaday.com/2011/09/20/roland-808-synced-to-midi/)，一辆 [TB-303](http://hackaday.com/2008/06/30/tb-303-teardown/) 和 [TR-909](http://hackaday.com/2008/06/18/tr-909-teardown/) 都是拆机的对象。