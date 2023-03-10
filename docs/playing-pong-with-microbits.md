# 用 Micro:bits 玩 Pong！

> 原文：<https://hackaday.com/2018/04/30/playing-pong-with-microbits/>

如果没有 Pong，这个世界会变成什么样，或许会少很多乐趣？对于像[Linker3000]这样的人来说，这款游戏是一种启发，可以教下一代黑客使用 [Micro:bits 作为控制器](https://github.com/linker3000/Microbit-TVPong)来构建和玩他们自己的版本！

为了尽一切努力，[Linker3000]说代码可以简单地上传到一个 Arduino 上，也就是你自己组装一个电路，如果你想直接开始工作的话。对于车间环境，这种设置使用复合视频输出，但这应该不是问题，因为大多数电视仍然保留这些输入。

一旦建成——或上传草图——Micro:bit 拨片就可以连接到 ATmega328p，像老式控制器一样播放，但[Linker3000]已经通过 Bitty 应用程序实现了对拨片 A 和 B 按钮的蓝牙控制。此外，如果你真的不喜欢有线电视，而蓝牙又太新，不适合这么老的游戏，那么第二个 Micro:bit 可以使用内置无线电控制有线球拍，前提是它们进行了相应的配置。

除了 Pong，还有壁球和足球游戏模式！休息后请欣赏演示。

 [https://www.youtube.com/embed/jDqk6mIApZk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jDqk6mIApZk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



关于微控制器电路、不同版本、将游戏区域绘制到屏幕上以及更多内容的详细描述，可以在他的[网站上找到，这里是](http://searle.hostei.com/grant/AVRPong/index.html)。这是一项令人印象深刻的事业，你必须尊重这样一个游戏的血统，但你知道他们说什么——[要么做大，要么回家](https://hackaday.com/2016/09/10/giant-scale-physical-pong/)。

[通过 [/r/Micro_Bit](https://www.reddit.com/r/Micro_Bit/comments/80khqn/play_the_classic_pong_game_on_a_tv_using_bbc/)