# 逆向工程一个盗版任天堂街机板

> 原文：<https://hackaday.com/2018/01/12/reverse-engineering-a-pirate-nintendo-arcade-board/>

任天堂 VS 系统是一个基于任天堂娱乐系统(NES)硬件的投币式街机系统。由于与家用游戏机关系如此密切，它使得在两者之间来回移植游戏变得很容易。作为一个街机系统，盗版游戏板和游戏有很大的经济动机，许多年后，这样一个盗版游戏板出现在[kevtris]，[的办公桌上，他决定对它进行逆向工程，以获得我们的观看乐趣。](https://www.youtube.com/watch?v=g8gZT1F9UkE)

有问题的主板运行超级马里奥兄弟，而不是使用实际的任天堂硬件，而是依赖于标准的 MOS 6502 来重建原始 CPU 的所有功能。Z80 也被投入使用，以模仿原始的音频硬件。由于 TTL 逻辑芯片中重新创建了许多功能，电路板功耗很高，上电时仅消耗 3 安培。我们想知道这些机器的消防安全，这些机器都被塞进了一个闷热潮湿的拱廊里。

[kevtris]在系统逆向工程方面做得很好，甚至为盗版板提供了完整的 PDF 原理图。一个老式的 SEGA 控制器被手工连接到棋盘上，既可以控制游戏，又可以作为硬币开关来玩游戏。

我们很想听听这些机器实际上是如何产生的故事，以及相关的设计过程，但目前来看，这可能会成为一个时代。大型公司多年来一直在打击街机盗版，并取得了不同程度的成功—[,我们在](https://hackaday.com/2017/12/19/drm-workarounds-save-arcade-cabinet/)之前已经看到过街机 DRM 被黑。

【感谢 Jero32 的提示！]

 [https://www.youtube.com/embed/g8gZT1F9UkE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/g8gZT1F9UkE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

