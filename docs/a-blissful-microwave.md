# 幸福的微波炉

> 原文：<https://hackaday.com/2017/02/10/a-blissful-microwave/>

[Tim]他的微波炉有问题。蜂鸣器特别烦人，一旦他的热口袋或比萨饼卷做好了，蜂鸣器就不会关闭。一种两千赫兹的音调感染了他的灵魂。这是唯一的声音回荡在一个波斯尼亚的噩梦重新加热冷冻食品。

不像存在主义的厌倦，微波炉里烦人的蜂鸣器是任何人都可以修理的。[Tim]拿了一把钳子去拿蜂鸣器，把它从印刷电路板上扯了下来。这给他留下了另一个问题——如何判断他的食物什么时候做好了。通过将 Windows XP 启动声音放入他的微波炉，这个问题得到了解决。

随着蜂鸣器的响起，[Tim]拿起一台 Arduino nano，用 Windows XP 启动声音加载它。Arduino 上没有太多的闪光灯，但它可以容纳 18kB 的样本，足以播放 8kHz 的启动声音。声音本身是 PCM 音频，很容易[塞进草图](https://github.com/TimGremalm/MicroMute)。

Arduino 监听微波炉产生的 2kHz 音调，并通过一个微型 D 类放大器发送 XP 启动声音。在微波炉里安装了扬声器后，[Tim]就有了一个非常蒸汽的微波炉。

 [https://www.youtube.com/embed/2EhFpzSXA9Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2EhFpzSXA9Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[通过 T0 黑客攻击。io]t1