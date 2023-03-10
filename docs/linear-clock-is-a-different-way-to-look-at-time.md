# 线性时钟是看待时间的一种不同方式

> 原文：<https://hackaday.com/2018/05/25/linear-clock-is-a-different-way-to-look-at-time/>

时钟通常有两种广泛的用户界面。一方面，你有表盘时钟，几个世纪以来的默认显示，它有编号的表面和旋转的指针。另一种模式是某种形式的数字时钟，当前时间直接显示为字母数字字符。它们都是时间的有用表示，但都有其局限性。

这是第三个模型——线性时钟。[Jan Derogee]想出了这个主意，这要归功于与其他类型时钟的一些可疑冲突的启发；我们觉得[这个介绍视频](https://www.youtube.com/watch?v=RGvCIdWW_QY)是用舌头牢牢地插在脸颊上制作的。不管灵感是什么，我们发现这个想法很聪明，而且执行得很好。时钟的运转装置只是一根长长的 M6 螺纹杆和一个步进电机。连接到螺母上的指针骑在杆上，随着步进器旋转它而移动。竖杆两侧有刻度，上午的时间在左边，下午的时间在右边。螺杆向一个方向旋转 12 小时，然后切换到另一个方向；当旋转角度改变时，指针会自动旋转到正确的刻度。对于报警器，[Jan]在每个刻度上都有黄铜棒，与指针接触；当他们遇到滑动的塑料绝缘体断开接触时，就会触发警报。ESP8266 控制一切，并播放警报的音频文件。

不寻常的时钟似乎是一件事。他的其他作品包括[这个整洁的磷光时钟和 YouTube subs 计数器](https://hackaday.com/2018/04/05/persistence-of-phosphorescence-clock-displays-youtube-stats-too/)，它肯定会随着这个时钟一起转动。

 [https://www.youtube.com/embed/O9em8ayWZjU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/O9em8ayWZjU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

