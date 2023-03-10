# 遥控发射器侵入音乐播放器

> 原文：<https://hackaday.com/2018/03/14/rc-transmitter-hacked-into-music-player/>

现代 RC 发射机配备了数量惊人的硬件，并且越来越有可能运行开源固件，实际上它本身就是一台多用途计算机。因此，有一个小的，但不断增长的，开发人员社区，推出了针对这些开关装饰的奇迹的软件应用程序。他们的末日来临只是时间问题。

[![](img/1c872a5d5c1e920a8fe2089a162e061a.png)](https://hackaday.com/wp-content/uploads/2018/03/rcmusic_detail.png) 一个这样的软件是 [TaraniTunes，由【吉尔德夫】](https://github.com/GilDev/TaraniTunes)开发。该程序允许您将音乐文件加载到配有 OpenTX 2.2+的 Taranis Q X7 或 Taranis X9D，这些文件可在发射器的内置扬声器上播放。虽然它可能不会赢得任何界面设计奖，但大液晶显示屏加上收音机的众多物理按钮和开关，使它相对容易地浏览您的音乐收藏。

虽然[GilDev]为 OpenTX 编写的软件看起来很简单，但让歌曲在收音机上播放却是另一回事。对于每个音轨，你需要将立体声声道合并成单声道(因为发射机只有一个扬声器)，然后将其转换成 32 kHz 的 WAV。但是不要担心缺少 ID3 标签信息，TaraniTunes 允许您创建一个文本文件，不仅包含每个曲目的文件名，还包含其名称和艺术家。

我们承认这个应该被归入“因为我能”一类，但它仍然是一个令人印象深刻的黑客技术，也是 RC 发射器技术当前状态的巧妙展示。

 [https://www.youtube.com/embed/gCiody4izEs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/gCiody4izEs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

