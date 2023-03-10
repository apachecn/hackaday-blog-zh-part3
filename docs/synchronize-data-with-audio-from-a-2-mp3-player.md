# 从 2 美元的 MP3 播放器同步数据和音频

> 原文：<https://hackaday.com/2016/06/13/synchronize-data-with-audio-from-a-2-mp3-player/>

这里介绍的许多黑客都是复杂的独创性技艺，你可能会认为它们来自太空时代的实验室，而不是黑客的工作台。令人印象深刻的东西，但在硬币的另一面，一个好的黑客的本质往往只是一个简单而优雅的方式来解决一个技术问题使用聪明的横向思维。

以[drtune]的这个项目为例，他需要将一些灯光与 MP3 播放器的音频流同步，并希望将他的灯光控制与 MP3 文件存储在同一个 SD 卡上。可悲的是，他的串行控制 MP3 播放器模块只能播放卡上的音频数据，而他无法从中读取数据文件，因此似乎没有简单的方法。

他的解决方案很简单:意识到该模块有一个立体声 DAC，但有一个单声道放大器[，他将数据编码为音频 FSK 流，类似于当年调制解调器使用的音频 FSK 流，并将其应用于他的立体声 MP3 文件的一个通道](https://hackaday.io/project/12191-dfplayer-mp3-module-get-data-from-sd-card)。然后，他可以播放第一个频道的音乐，并将另一个频道的 FSK 数据数字化，然后将其应用于软件调制解调器以检索其信息。

不过有一个小问题，MP3 播放器在向放大器提供音频之前将两个声道相加。这并不是一个很大的问题，只需在器件数据手册中做一点探索工作，他就可以识别出进行混频的电阻网络，并移除数据通道的元件。

他在广告下方的视频中公布了该系统的全部细节，包括波形和免费播放的音频 FSK 数据。

 [https://www.youtube.com/embed/1ay75rPWEeM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1ay75rPWEeM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



这不是我们第一次在 Hackaday 展示音频 FSK 数据。我们已经报道了它使用[从 8 位计算机](http://hackaday.com/2016/04/12/dump-your-old-computers-rom-using-audacity/)中检索 rom，看到它作为电视新闻直升机报道的一部分出现在[中，甚至看到](http://hackaday.com/2014/02/02/decoding-news-helicopter-signals-on-youtube/)[一台国家安全局的克雷超级计算机在用作*星际旅行*音效时用来解码它](http://hackaday.com/2016/01/13/decoding-data-hiding-in-star-trek-iv/)。