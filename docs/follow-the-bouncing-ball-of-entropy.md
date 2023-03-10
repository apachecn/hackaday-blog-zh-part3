# 跟随熵的弹跳球

> 原文：<https://hackaday.com/2017/09/01/follow-the-bouncing-ball-of-entropy/>

当[::vtol::]想要生成随机数时，他不是简单地在他的 Arduino IDE 中键入 rand()，不，他创建了一个艺术作品。这一切都始于一个旋钮，大概是连接到一个电位计，它设置一个频率。Arduino UNO 读取读数，并为朝上的扬声器生成音调。一个小球在扬声器上反弹，偶尔会与压电元件发生碰撞。碰撞之间的时间间隔成为我们的足够的随机数。

生成的数字沿着 Rube Goldberg 式的机器向上传输到安装在顶部的 LCD 上，在那里显示一个与我们生成的数字相对应的单词。只要按钮被按住，音调将继续响起，单词将产生，因此诗歌涌出。

如果这种对垮掉的诗歌的追求不适合你，Ball-O-Bol 的构造具有引人注目的美学品质，而像他的[听地板的磁带头机器人](https://hackaday.com/2016/12/18/tape-head-robot-listens-to-the-floor/)和 [8 位数码照片枪](https://hackaday.com/2015/04/03/8-bit-digital-photo-gun/)这样的项目显示了电子内脏的前端和中心，具有自己的吸引力。

[https://player.vimeo.com/video/230886150](https://player.vimeo.com/video/230886150)