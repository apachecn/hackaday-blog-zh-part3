# Hackaday 奖参赛作品:痴呆症友好型音乐播放器

> 原文：<https://hackaday.com/2017/09/15/hackaday-prize-entry-dementia-friendly-music-player/>

失去记忆是一种极其困难的情况，不仅对那些受折磨的人来说如此，对直系亲属、密友和照顾者来说也是如此。由于痴呆症无法治愈，提供护理对每个人来说都是一项极其艰巨的任务——无论是精神上还是身体上。患者无法记住最近的事件和信息，但很可能能够回忆起一些过去的记忆。当他们遇到“现代”技术，并且不知道如何使用和操作正常人认为理所当然的日常设备时，这就提出了严峻的挑战。

[rosswesleyporter]的父亲在使用现代 iPods 和 CD 播放器方面有困难，所以他建造了[DQMusicBox——一种对痴呆症友好的音乐播放器](https://hackaday.io/project/26096-dementia-friendly-music-player)。这是一个非常简单的界面，类似于半个世纪前的收音机。只有两个大的、标记清晰的转盘——一个用于调节音量，另一个用于调节歌曲，还有一个耳机插孔。灵感来自一部非常感人的纪录片《内心世界》，这部纪录片探索了音乐如何给痴呆症患者带来极大的快乐。

该设备是围绕一个树莓皮构建的，封装在一个激光切割外壳中，不需要焊接——使任何人都可以使用容易获得的部件轻松为自己构建一个。Raspberry Pi 运行在一个轻量级的优化版 Raspbian 上，名为 DietPi。音乐播放由 VLC 处理，确保支持大量的音乐格式。Python 脚本查找音乐文件，设置 VLC-NOX 播放器，并处理旋钮和按钮事件。该软件的捆绑映像文件包括运行该软件所需的一切，使安装变得简单快捷。由于 Raspberry Pi 在没有正确关机的情况下断电时容易损坏操作系统，[Ross]在 SD 卡上使用写保护，并带您了解它的工作过程。

在他的[项目页面](https://hackaday.io/project/26096-dementia-friendly-music-player)、 [Github](https://github.com/rosswesleyporter/dqmusicbox) 和 [DQMusicBox 网站](https://dqmusicbox.com/)之间，你将能够获得复制这个优秀项目所需的所有信息。对于他的下一个版本，他已经有了一些改进的想法，并希望听到其他黑客是否有建议。

 [https://www.youtube.com/embed/jL_30Z0DFKY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jL_30Z0DFKY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)