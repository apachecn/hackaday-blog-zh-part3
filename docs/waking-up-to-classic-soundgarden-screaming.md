# 醒来时听到经典的声音花园乐队尖叫

> 原文：<https://hackaday.com/2018/05/07/waking-up-to-classic-soundgarden-screaming/>

在这位歌手于 2017 年英年早逝之前，这个项目实际上只有*稍微*不那么令人毛骨悚然，[这款由【Rafael Mizrahi】](https://www.youtube.com/watch?v=8s6xB8kiXe0)制造的闹钟会在随机选择的克里斯·康奈尔标志性尖叫声中唤醒用户。他不满足于仅仅局限于体验的音频部分，他将所有的硬件都装在一个聚苯乙烯泡沫塑料头内，并配有一张打印出来的歌手的脸。

[![](img/dd77bf128995a31a16cdf252bf6034c5.png)](https://hackaday.com/wp-content/uploads/2018/05/cornell_detail.jpg) 一个 Arduino Uno 加上一个七段 led 显示屏提供时钟本身，它位于底座上。没有 RTC 模块，所以 Arduino 尽最大努力通过计算毫秒来保持时间。这意味着时钟会漂移很大一段时间，但是考虑到除了编辑源代码之外，没有设置时间或更改时间的规定，看起来准确的计时对于这个项目来说并不是非常重要。

音频由一个 [Adafruit VS1053](https://www.adafruit.com/product/1381) 提供，它包含一个 microSD 卡，里面装满了康奈尔唱歌的 MP3 样本。这是连接到一个 X-Mini 便携式胶囊扬声器，安装在一个中空的泡沫部分。

非常规闹钟是 Hackaday 的主要产品。从对你进行身体攻击的场景到用 OLEDs 模仿日出的 T2 场景，我们认为我们已经看到了一切。我们错了。

 [https://www.youtube.com/embed/8s6xB8kiXe0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8s6xB8kiXe0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

