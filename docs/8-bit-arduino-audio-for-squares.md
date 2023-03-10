# Hackaday 奖品:8 位 Arduino 音频，用于 Squares

> 原文：<https://hackaday.com/2016/06/12/8-bit-arduino-audio-for-squares/>

一台普通的 Arduino 并不以其高保真音频生成能力而闻名。对于像样本回放这样的“严肃”音频，人们通常会添加一个带有硬件的屏蔽来完成繁重的工作。如果做不到这一点，许多项目将自己限制在恒定音量的方波，这在音乐上是缺乏灵感的，但这很容易。

[Connor]为 Arduino 设计的[音量控制方案](https://hackaday.io/project/11957-8-bit-component-less-volume-control-for-arduino)填补了这一空白。他从制造那些无聊方波的[音库](https://www.arduino.cc/en/Reference/Tone)开始，[增加了动态音量控制](https://github.com/connornishijima/arduino-volume)。区别很容易听出来:在自然界中，几乎没有声音是瞬间开始和结束的。敲一下锣，它就响了，同时变得越来越安静。这就是[Connor]的代码让你用 Arduino 做的事情，而你只需要做很少的额外工作。

演示视频附带的代码(嵌入在下面)是一个很好的起点。例如，Gameboy/Mario 的声音就像播放两个音调一样简单，让第二个逐渐消失。尽管如此，这听起来很棒。

在幕后，它使用定时器 0 以最大速度创建“模拟”值(通过 PWM 和`analogWrite()`命令),使用定时器 1 创建音频速率方波。就这样，真的，但也够了。很多受人喜爱的经典街机游戏并没有做得更多。

虽然你可以用同样的硬件做更奇妙的事情(比如[样本回放](http://hackaday.com/2016/02/12/embed-with-elliot-audio-playback-with-direct-digital-synthesis/)),但是音量包络方波方法很容易编写代码。如果你想要给你的机器人一些简单的，听起来像机器人的声音效果，我们真的很喜欢这种方法。

 [https://www.youtube.com/embed/4wkMY6DDPDw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/4wkMY6DDPDw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2016](http://hackaday.io/prize) is Sponsored by: [![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](http://hackaday.io/atmel)  [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](http://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](http://www.digikey.com/)  [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](http://supplyframe.com/)