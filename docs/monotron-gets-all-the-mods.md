# Monotron 得到所有的模块

> 原文：<https://hackaday.com/2018/06/09/monotron-gets-all-the-mods/>

[Harry Axten]将小巧的[Korg Monotron 变成了可播放的模拟合成器](http://harryaxten.altervista.org/monotronkb.html)，配有一个跨越两个八度音阶的全尺寸键盘和一个 MIDI 接口。

Korg 早在 2010 年就推出了 Monotron 模拟迷你合成器。他们还[放弃了合成器的原理图](https://hackaday.com/2010/11/10/monotron-openly-monophonic/)。黑客们没有浪费时间修改和改进 Monotron。[Harry]将这些变化融入了他的构建中。低频振荡器(LFO)已改为包络发生器。ribbon 控制器不见了，取而代之的是声音音符的 CV/gate 接口。

CV/gate 接口依次连接到 ATMega328P，atmega 328 p 将其转换为 MIDI。MIDI 数据来自两个来源之一:从废弃的 MIDI 控制器中拉出的两个八度全尺寸键盘或后面的 MIDI 连接器。

用户界面不仅仅停留在键盘上。原来 Monotron 上的低成本 pots 已被前面板上质量更高的部件所取代。调音壶是一个 10 圈的装置，允许精确调音。所有的模块都安装在一个单板上，这个单板连接到原来的 Monotron 板。

所有辛勤工作的成果是一种演奏起来非常有趣的乐器。看看下面的视频吧。想要更多吗？你可以阅读所有关于 Monotron 的哥哥 Monotribe 的黑客攻击。

 [https://www.youtube.com/embed/TdBuLwyNlp0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/TdBuLwyNlp0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

