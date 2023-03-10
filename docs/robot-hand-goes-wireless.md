# 机器人手无线化

> 原文：<https://hackaday.com/2017/03/13/robot-hand-goes-wireless/>

我们无法决定[MertArduino 的] [机器人手项目](http://www.instructables.com/id/Arduino-Make-a-Low-Cost-Robotic-Hand-With-Wireless/)是更艺术还是演示项目。使用弹簧、钓鱼线和伺服电机的结构不会给你一只实用的手来抓住或操纵任何重要的东西。然而，该项目展示了许多有趣的构建技术，并且是在项目中使用 nRF24L01 无线的有趣演示。你可以在下面看到这个装置的视频。

一只手套使用自制的柔性传感器向手发送无线命令。另一个 Arduino 驱动一系列伺服电机，使手指弯曲。你没有很好的控制，也没有真正的握力，但是手或多或少会重复你的动作。我们注意到一个手指似乎控制不好，但我们怀疑这是一个自制的弯曲传感器变红。

flex 传感器很巧妙，但可能不太可靠。它们由一根短软管、一个 LED 和一个光敏电阻组成。我们猜测很多因素可能会改变弯管周围的光量，这可能就是视频中一根手指的问题所在。

我们很乐意使用一些[导电袋弯曲传感器](https://hackaday.com/2012/06/04/making-flex-sensors-on-the-cheap/)尝试这个项目。虽然这只手看起来不像抓具，但我们想知道它是否可以用于[手语项目](https://hackaday.com/2017/03/02/speech-to-sign-language/)。

 [https://www.youtube.com/embed/5z5evInThP4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5z5evInThP4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

