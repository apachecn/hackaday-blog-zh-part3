# 使用十进制计数器使发光二极管闪烁

> 原文：<https://hackaday.com/2017/07/22/using-a-decade-counter-to-make-leds-flash/>

[安德里亚·德·那波利]创造了一个由半打 LED 组成的 [LED 显示屏，连接到 CD4017 十进制计数器的反向信号，给人一种黑暗 LED 来回运行的效果。CD4017 通过激活 10 个输出来工作，一次一个，由发送到引脚 14 的时钟信号控制。](https://hackaday.io/project/25901-running-led)

在 PNP 晶体管和 12K 电阻的帮助下，第一个和最后一个 led 由输出 0 和 5 点亮。中间的四个 led 由两个输出切换，当其中一个输出变高时，led 变暗。[Andrea]深入研究了 CD4017，他在项目页面分享了许多细节。

Hackaday 发布了很多关于晦涩难懂的 IC 的帖子:Project 54/74 旨在创建一个 5400 和 7400 系列 IC 的管芯图像[数据库。在一首经典歌曲的混音版中，](http://hackaday.com/2017/04/04/project-5474-maps-out-logic-ics/) [Baby 10 使用 4017 来制作音乐音序器](http://hackaday.com/2016/01/14/oh-baby-baby10-build-a-classic-analog-music-sequencer/)。

 [https://www.youtube.com/embed/-Sn0L-40nmQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-Sn0L-40nmQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

