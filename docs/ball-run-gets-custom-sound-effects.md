# 球跑获得自定义音效

> 原文：<https://hackaday.com/2016/06/13/ball-run-gets-custom-sound-effects/>

建造一条大理石跑道一直在我的项目清单上，但现在我不得不修改这个计划。除了建造一条有趣的轨道让球体穿越之外，[杰克·阿泽顿]还添加了由弹球触发的定制音效。

我在斯坦福大学音乐和声学计算机研究中心的 Maker Faire 展位上遇到了杰克。这很拗口，所以他们通常用缩写 CCRMA。除了他的项目之外，还有许多其他的项目在展出，所有的项目都有一个简短的评论供你欣赏。

[杰克]称他的项目为*飞跃深渊*，与[同名，轨道是仿照](https://en.wikipedia.org/wiki/Leap-The-Dips)设计的过山车。这是我第一次听说通过游乐园的游乐设施来铺设滚动球雕塑轨道，但这很有意义，因为保持球滚动的工程已经完成了。弯曲粗规格电线后，用无铅焊料和喷灯将其固定到位。

如前所述，该项目并没有就此停止。他添加了四个压电元件，由 Arduino 板监控。每一个都在轨道的一个特别极端的倾角，这使得很容易检测到弹珠滚动过去。与电脑的 USB 连接允许 Arduino 触发 MaxMSP 补丁来播放声音效果。

为了演示，Faire 观众在让球滚动的同时戴着耳机，但在下面的视频中[Jack]让我直接插入他的 Macbook 上的耳机端口。这有点奇怪，因为在这一部分没有集会的背景声音，但这是我能得到合理录音的唯一方法。我喜欢这种效果，并且认为使用[Teensy 音频库](http://hackaday.com/2014/09/30/the-teensy-audio-library/)和音频适配器硬件将它包装成独立的会非常有趣。

 [https://www.youtube.com/embed/-aVVq45W7VY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-aVVq45W7VY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

