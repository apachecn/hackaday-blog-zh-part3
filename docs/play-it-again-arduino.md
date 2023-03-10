# 阿杜伊诺，再放一遍

> 原文：<https://hackaday.com/2017/07/23/play-it-again-arduino/>

[MrRedBeard]想要播放 Arduino 程序中的一首特定歌曲，并且厌倦了尝试手动转录音符。一项小小的研究发现，有一个项目将音乐 XML (MXL)文件转换成 Arduino。然而，[红胡子先生]并不喜欢它所使用的语言，所以他[创造了自己的方法来做同样的事情](http://www.instructables.com/id/Translate-Songs-to-Be-Played-on-Arduino/)。他一路上学到了很多东西，并愿意在教程中分享，如果你想做同样的事情，这将有助于你。你可以在下面看到他的结果的视频。

当然，如果你必须手工创建，MXL 文件可能并不比乐谱好。幸运的是，网上有一个很大的收藏库，里面有你感兴趣的歌曲。请注意，[Mr red beard]帖子中的链接错误地将该网站作为. com 而不是. org，因此您将希望在这里而不是那里使用该链接。

一个 [C#应用程序](https://github.com/MrRedBeard/DotNet-MXL-Parsing-for-Arduino)读取 MXL 文件并转换它以便在 Arduino 上使用。这里也有 Arduino 的[样本代码来帮助你入门。](https://github.com/MrRedBeard/DotNet-MXL-Parsing-for-Arduino/blob/master/Arduino%20Sample%20Code)

启发他的项目在 GitHub 上，如果更适合你的话，可以使用 Ruby。顺便说一下，我们之前已经讨论过 [MXL](https://hackaday.com/2017/05/25/taming-those-music-reading-demons/) 。如果你想在 Arduino 上集成多声道音乐，你可以在这里开始。

 [https://www.youtube.com/embed/GPvD2ShnI3s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/GPvD2ShnI3s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

