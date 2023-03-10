# LED 条形显示屏为您提供了两种欣赏音乐的方式

> 原文：<https://hackaday.com/2017/01/17/led-strip-display-gives-you-two-ways-to-see-the-music/>

这个 LED 条形音乐可视化器是一个难题。它随着音乐点亮并跳动，类似于 20 世纪 70 年代迷幻音乐的光器官，但不仅仅如此。它更像是大卫·霍索夫乘坐的《T2 骑士 T3》前面的拉森扫描仪吗？有一点，但不完全是。

无论你决定如何称呼这个东西，它看起来都很酷，斯科特·劳森提供了两种方式来建造它。企业端是一条简单的 WS2812b 可寻址 led。看起来该项目的第一个化身是一个 ESP8266 驱动 led，以响应运行可视化代码(用 Python 编写)的 PC 发送给它的命令。这种设置将计算密集型可视化代码与显示器分开，但将显示器限制为 256 像素，并且可能必须处理网络延迟。Raspberry Pi 版本既处理数字又驱动显示，但 Pi 不具备运行 led 和 GUI 的能力，这本身就很有趣。下面的视频展示了不同的可视化模式——我们倾向于最后的“能量效果”。

挑选你的硬件，为你的下一次狂欢扔几个这样的东西在一起。如果你需要更多关于上述拉森扫描仪的背景知识，[我们已经为你准备好了](http://hackaday.com/2014/11/17/larson-scanner-namesake-glen-larson-passes-away/)。

 [https://www.youtube.com/embed/HNtM7jH5GXg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HNtM7jH5GXg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[via [r/raspberry_pi](https://www.reddit.com/r/raspberry_pi/comments/5m8htn/realtime_led_strip_music_visualization/)