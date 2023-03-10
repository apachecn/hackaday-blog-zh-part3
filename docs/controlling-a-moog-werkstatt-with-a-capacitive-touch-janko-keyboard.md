# 使用电容式触摸 Jankó键盘控制 Moog Werkstatt

> 原文：<https://hackaday.com/2017/06/08/controlling-a-moog-werkstatt-with-a-capacitive-touch-janko-keyboard/>

亚特兰大 Freeside 的成员 Ben Bradley 为佐治亚理工学院 Moog 黑客马拉松制作了一个[电容式触摸 Jank 键盘](http://blog.freesideatlanta.org/2017/02/a-capacitive-touch-janko-keyboard-what.html)。 [Jankó键盘](https://en.wikipedia.org/wiki/Jank%C3%B3_keyboard)是 19 世纪增加更紧凑钢琴键盘的尝试。琴键数量是传统钢琴的三倍，但垂直排列(据说)在演奏时更方便——一只手可以覆盖整个八度音阶。但是，是的，它从来没有流行过。

[Ben]的项目由一系列连接到 Adafruit 电容触摸分线板的黄铜片组成，Arduino Mega clone 的四个 I2C 地址各有一个。触摸按键时，Arduino 向 Werkstatt 发送按键信号，同时使用 R-2R 梯形电阻为 VCO 指数输入产生电压。

最近的 Moog 黑客马拉松是第三次。仅佐治亚理工学院就有 25 个团队参赛，还有更多来自其他学校的团队，[工作 48 小时](https://music.gatech.edu/hackathon-recap-2017)与 Moog Werkstatt-1 模拟合成器建立接口，争夺 5000 美元的现金奖励以及前三名团队的 Werkstatt。

我们是黑客日的合成器爱好者:我们涵盖了从[模拟合成器](http://hackaday.com/2017/02/24/a-mess-of-wires-turned-into-an-analog-synth/)到[压控滤波器](http://hackaday.com/2017/04/25/old-part-day-voltage-controlled-filters/)的一切。

Via [Freeside Atlanta](http://blog.freesideatlanta.org/) ，照片由[内森·伯纳姆](https://goo.gl/photos/zKLTUZwC7X6PeG4F7)拍摄。

 [https://www.youtube.com/embed/gPpw7xp3CDY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/gPpw7xp3CDY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

