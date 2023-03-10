# 两人份的茶:一个小小的茶计时器

> 原文：<https://hackaday.com/2017/03/11/tea-for-two-a-tiny-tea-timer/>

ATtiny85 微控制器什么都没有:8 KB 的闪存，8 位架构，只有 8 个引脚(其中 3 个负责电源和复位)。这正是它非常适合小型项目的原因。

[Mimile]的[茶定时器](https://hackaday.io/project/20175-tea-timer)有一个开关、一个按钮、八个发光二极管和一个蜂鸣器。将开关拨到“设置”位置，按下按钮运行所需的浸泡时间。把它翻转到“跑”，你就开始计时了。发光二极管闪烁，蜂鸣器发出“两人份的茶”的方波。精彩！

但是，等等，如何仅用五个引脚来控制所有这些 I/O？两个开关各一个引脚，蜂鸣器一个引脚，这样就只剩下两个引脚用于八个 LED 显示器。【Mimile】好玩的解决方法是用一个二进制计数器(a 74HC393)和剩下的两行进行计数和复位。这意味着快速切换一个引脚 255 次，以点亮所有的 led。这是一种奇怪的方式，但我们喜欢它！

事实证明，Hackaday 无法抵挡 ATtiny85 的诱惑。无论是[教它发誓](http://hackaday.com/2015/10/21/teach-an-attiny-85-to-swear/)、[说 I2C 语](http://hackaday.com/2016/11/07/diy-i2c-devices-with-attiny85/)，还是[传输模拟电视信号](http://hackaday.com/2015/02/26/attiny85-does-over-the-air-ntsc/)，这个可爱的小芯片总有一些东西邀请你[测试你的勇气](http://hackaday.com/2015/12/17/attiny-does-170x240-vga-with-8-colors/)。