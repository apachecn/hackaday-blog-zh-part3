# 为了更大的正义，重新使用教室响片

> 原文：<https://hackaday.com/2016/12/04/repurpose-a-clicker-for-great-justice/>

如果你在某个规模的大学课堂上，和一个想从学生那里获得实时反馈的教授在一起，你可能会被迫购买一个转折点“响片”。除了让学生为他们教授的教学助手付费的荒谬之外(这也让你为粉笔额外付费了吗？！？！)这些响片对任何有头脑的黑客来说都是一个挑战，因为它们可能包含秘密。

[Nick]有一个这样的小玩意，他跳上巨人的肩膀，把它变成一个与他的电脑接口并驱动合成器的[遥控器，这样他就可以通过点击来改变和弦。他两次提到](https://nickmooney.com/lecture-clicker-synthesizer/)[【特拉维斯·古斯比】的 nRF 滥交黑客](https://travisgoodspeed.blogspot.de/2010/07/reversing-rf-clicker.html)和[【泰勒·基利安】的用于遥控器的 Arduino 库](http://www.taylorkillian.com/2012/11/turning-point-clicker-emulation-with.html)，这证明了为什么我们既需要逆向工程师做艰苦的工作，也需要那些将艰苦的工作打包到一个易于使用的库中的人。

就这样，真的。[Nick]将 Arduino 连接到 nRF24，将 clicker 的解码输出发送到他的计算机，并编写 Python 例程，通过 MIDI 将他想要的任何音乐播放到基线合成器。整个射击比赛[在 GitHub](https://github.com/nickmooney/turning-clicker) 上有。如果你有一个遥控器在某个地方积了灰尘，把它拿出来做点什么。