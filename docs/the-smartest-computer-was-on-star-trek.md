# 最聪明的电脑在《星际迷航》上

> 原文：<https://hackaday.com/2017/02/11/the-smartest-computer-was-on-star-trek/>

电视和电影里出现了很多智能电脑。然而，我们通常认为最聪明的是《星际迷航》中的那些人。不是大型的“图书馆电脑”，也不是小型的银色便携式电脑。不,《星际迷航》里的智能电脑控制了门。如果你曾经观察过，门似乎知道有人走向它和有人在拳赛中飞向它之间的区别。它似乎也知道什么时候有更多的人在去门口的路上。

当然，它们如此智能的原因是这些门真的是由人来操作的。不过，对于真正的粉丝来说，你可以从企业购买一个看起来像对讲机面板的小工具。那会很酷，但是这个有声音效果，当有人走进你的门口时可以感觉到，所以他们可以听到涡轮电梯门令人安慰的嗖嗖声。

当然，对于真正的黑客来说，那也不够好。[Evan]从这个 25 美元的小工具开始，但想用 Arduino 控制它，以包含在他的 hackerspace 的气动门系统中。他做了一点逆向工程，一点编码，他完成了对设备的完全控制。

该设备的内部结构非常简单，包括一些 PIR 传感器、开关、led 和一些产生声音并控制逻辑的环氧树脂块。[埃文]必须有点创意，因为红色警报声音，一旦开始，将不会停止一段时间。解决办法？当 Arduino 想要安静的时候，让它切断电路板的电源。

该代码可在 [GitHub](https://github.com/abzman/star-trek-panel) 上获得。还需要一些其他技巧，包括移除 PIR 传感器芯片和添加 USB 到串行适配器。一旦你能把整个东西当作一个 I/O 设备，你可能会很容易地做很多有趣的项目。当然，这种产品作为[黑客日科幻竞赛](https://hackaday.io/contest/19541-hackadays-2017-sci-fi-contest)的参赛作品将是完美的。

 [https://www.youtube.com/embed/hcOiNBp1J68?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hcOiNBp1J68?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



出于某种原因，我们没有看到像下一代那样多的原创系列黑客。不过，我们已经看到了至少另一个 [swoosh 门](https://hackaday.com/2011/11/27/star-trek-style-pneumatic-doors-that-dont-require-a-stagehand/)。另一方面，如果你被一个柯克船长式的身体撞向那扇门，门仍然会打开。我们不能保证这一点，但这个视频有一个有趣的门噪音分析，让我们想起了一个现代版的播放我们的旧唱片。