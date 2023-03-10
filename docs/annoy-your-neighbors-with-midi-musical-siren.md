# 用 MIDI 音乐警报器骚扰你的邻居

> 原文：<https://hackaday.com/2017/01/29/annoy-your-neighbors-with-midi-musical-siren/>

[Yannick]，又名[Gigawipf]为我们带来了这种(大部分)音乐美食:一个由无刷四轴马达驱动的 [3D 打印警报器](https://hackaday.io/project/19525-using-a-siren-as-midi-intrument)，能够播放(大部分)任何你有 MIDI 乐谱的音乐。这是一个神奇的 quickie 项目，对于任何一个有一个坏掉的 quad，甚至一些备件和一台 3D 打印机的人来说。尽管有明显的难度，这实际上会是一个很好的快速周末构建。

第一站是 Thingiverse，为[迷你空袭警报模型](http://www.thingiverse.com/thing:1534397)。开始印刷，并着手研究电子设备。对于 MIDI 到 ESC(电子速度控制器)的转换，任何支持 USB 的 Arduino(atmega 32 u 4 或 ARM 板)都可以工作。重要的是你可以运行 [MIDI-USB 库](https://www.arduino.cc/en/Reference/MIDIUSB)。剩下的只是一个 MIDI 到伺服脉冲的转换和查找表。[这是【亚尼克】的文件](https://github.com/Ultrawipf/midiSiren/blob/master/midiSiren.ino)，但是我们猜测你会想要调整你自己的警报器。

效果如何？请看下面的视频。短音符，以及音符关，税收四电机的能力，立即停止警报器转子。有一个很好的滑音效果，因为它在音符之间上升。你需要相应地选择你的曲目。

我们对音乐警笛有一种奇怪的亲近感，所以我们很乐意承认【亚尼克】在“旋转”这个词上欺骗了我们。这是一个简单的项目，结果很酷。据我们所知，世界上只有一个 3D 打印的 MIDI 控制的警报器，但放大或缩小警报器模型以制作不同的音域和效果应该不难。那么谁想听这些东西的交响乐呢？

 [https://www.youtube.com/embed/IlCgn9LvN9c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/IlCgn9LvN9c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

