# USB 音量控制

> 原文：<https://hackaday.com/2015/11/22/usb-volume-control/>

如果你买了昂贵的电脑扬声器，它们通常有一个音量旋钮，你可以把它安装在桌子上的某个地方，这样你就不需要依赖内置的音量控制器了。[Kris S]决定打造自己的[版遥控音量控制器](http://www.instructables.com/id/Digispark-Volume-Control)。毫不奇怪，它使用了兼容 Arduino 的 Digispark 板和旋转控制器。Digispark(克里斯花 2 美元买的)与 Adafruit 小饰品兼容。这很关键，因为小饰品库使得通过 USB(使用 HID 接口)发送媒体密钥来控制音量变得容易。

不过，说真的，这个建筑最好的部分是由药瓶制成的好看的把手(见下面的视频)。micro Digispark 足够小，可以放入药瓶的盖子中，一些蜡和颗粒增加了音量控制的分量。

标准的 Arduino 库在发送多媒体键时有问题，但是在之前的一篇文章中，我构建了一个基于手势的音量控制，成功地实现了这一点。我们过去也报道过[类似的音量控制](http://hackaday.com/2013/11/14/cloning-the-trinket-for-a-usb-volume-knob/)。那个也很好看，但是比克里斯在这里做的更复杂。

 [https://www.youtube.com/embed/eCxZuw9RTrs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/eCxZuw9RTrs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

