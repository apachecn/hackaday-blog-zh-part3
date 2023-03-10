# 使用 HopeRF RFM69 的无线琐事游戏蜂鸣器

> 原文：<https://hackaday.com/2016/10/08/wireless-trivia-game-buzzers-using-hoperf-rfm69/>

电视游戏节目遵循一个六十年来没怎么变的公式。名人主持人、迷人的助理、流行语、俗气的胶合板布景、紧张的参赛者，当然还有嗡嗡声。

如果你想自己做一个小测验，很容易就可以省去主持人、助手、布景和口头禅，但是除了参赛者，你仍然需要蜂鸣器。你可以把过去电视技术人员藏在电视机里的电线弄得乱七八糟，但在你家里或酒吧里，这很快就会变得不方便。

[拉里]通过[建造一个无线蜂鸣器](http://amateurmachinemaster.blogspot.co.uk/2016/10/wireless-buzzers.html)解决了他的琐事游戏蜂鸣器问题。它采用 3D 打印外壳，包含 Adafruit Feather 微控制器，并使用 RFM69 900MHz 无线电模块代替电线。主单元在有机发光二极管屏幕上显示最快的参赛者，它的特点是在按键之间有一个低功耗待机模式以节省电池电量，并注意在按键时添加随机计时以避免碰撞。

按钮本身开始是一个 3D 打印的按钮，可以操作一个触摸开关，但在边缘按压无法激活单个开关后，移动到一组三角形的三个开关。

我们之前已经展示过[一个有线游戏节目蜂鸣器](http://hackaday.com/2012/02/03/office-game-show-buzzer-keeps-things-fair-and-square/)，但是为了完整的游戏节目体验，[这个倒计时器](http://hackaday.com/2015/06/05/nice-looking-countdown-timer-for-the-home-game-show-enthusiest/)怎么样？