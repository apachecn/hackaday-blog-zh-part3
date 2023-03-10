# 模块化鼓机创造随机节奏

> 原文：<https://hackaday.com/2016/07/09/modular-drum-machine-creates-random-rhythms/>

别担心，节奏本身并不是随机的！那很难成为有用的鼓机。[【kbob】的创作确实有随机生成功能性节奏](https://kbob.github.io/2016/06/27/i-made-this-drum-machine)的能力，不过这都是在试验板上完成的。

这个微型鼓机的核心是两块小小的开发板。一个是调频合成器，听起来像鼓，另一个是带有几个控制的随机节奏发生器。算法来自可变仪器公司的开源 Eurorack 模块。整个事情适合一个试验板与 JIGMOD 模块的用户界面。该机器依靠 USB 手机充电器形式的锂电池运行。电池座采用 Fusion 360 设计，3D 打印。

鼓机的功能也很有趣。机器上的按钮上有一组触发器。当按下按钮时，鼓机会在适当的时间播放声音，确保没有不正常的节拍。电位计每毫秒轮询一次，程序根据需要更新输出。还有一个节奏“网格”，由另外两个旋钮(一个用于映射 X 坐标，另一个用于映射 Y 坐标)和一个“混沌”按钮控制，该按钮为该映射添加了随机性元素。

这个项目的模块化性质将使这成为一个伟大的乐器添加到一个人的音乐曲目。它很容易定制，并且可以与任何一种[数量的其他合成器乐器](http://hackaday.com/2016/02/23/a-slew-of-open-source-synthesizers/)相适应。

 [https://www.youtube.com/embed/p0GLgOOg_Dg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/p0GLgOOg_Dg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

