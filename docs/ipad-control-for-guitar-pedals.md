# 吉他踏板的 IPad 控制

> 原文：<https://hackaday.com/2016/05/28/ipad-control-for-guitar-pedals/>

[gutbag]是吉他手。吉他手是臭名昭著的旋钮旋转者:他们喜欢他们的效果踏板。但是当你的音乐在一首歌中间多次改变设置时，会让人分心。要是在表演过程中有机器人小手可以转动旋钮就好了(抱歉，这是比喻)

[gutbag]打开他的 EHX 音叉踏板，发现所有的外部旋钮控制都被芯片上的 ADC 读取，并进行所有的处理。他用一个 DAC 和一些模拟开关取代了所有的控制，在 ATmega328 中编写了一些 MIDI 逻辑，并为自己建造了一个定制的 MIDI 控制的吉他踏板。非常巧妙，他现在可以用他的 iPad 现场控制它，或者用他们 MIDI 系统的其余部分控制旋钮。

[![2](img/8a421c8fcd59596287ad5858d20c1252.png)](https://hackaday.com/wp-content/uploads/2016/05/2.jpg)

然而，这并不是[gutbag]第一次涉足踏板自动化。他之前已经自动化了他的一系列踏板，这些踏板是用来接收控制电压信号的。我们喜欢这种方式的原因是 DAC 直接取代了电位计。只是更粗糙。(哦，我们还羡慕[gutbag]的实验室设置。)

这也不是我们第一次报道[gutbag]的乐队 Zaardvark 了。早在 2013 年，我们就报道过他们的[风琴踏板到 MIDI 的破解](http://hackaday.com/2013/06/25/tearing-apart-an-organ-and-making-a-midi-keyboard/)。继续摇滚。

 [https://www.youtube.com/embed/mtA1Rxf9oRY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mtA1Rxf9oRY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

