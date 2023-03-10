# 两个转盘，没有麦克风

> 原文：<https://hackaday.com/2015/11/09/two-turntables-and-no-microphone/>

过去，你必须花真金白银为你的电子音乐武器库换一个控制器。如今，有了便宜的微控制器和容易获得的免费软件库，你可以为口袋里的零钱做些了不起的事情。但这并不意味着你不能在这个过程中做出一件性感、实用的艺术品！[Jan Godde]用他聪明命名的带有两个转盘的木制传感器盒做到了这一点。(如果你有更好的名字，请在评论中提出来。)

![mpv-shot0003](img/e732f4e566fe1592afab3ee263884246.png)从我们所看到的，盒子有两个电位计滑块，两个触摸感应电位计，两个力敏电阻，一系列旋钮，和一整串(电容？)接触点。简而言之，在一个美观的盒子里有一吨各种尺寸和形状的连续控制器。但最引人注目的是，这款设备的名字来自于两个用作滚轮的旧硬盘。

如中断下方的视频所示，两个滚轮底部覆盖有交替的条纹。每个盘片下面都有一对专用的红外发光二极管和光电探测器，用作[正交编码器](https://en.wikipedia.org/wiki/Rotary_encoder#Incremental_rotary_encoder)，允许【Jan】判断盘片旋转的方向和距离。

[https://player.vimeo.com/video/144913718](https://player.vimeo.com/video/144913718)

我们喜欢两个滚轮与各种滑块结合使用的生动演示。挺有表现力的，喜怒无常。但是不要忽视了一堆(十个？十二个？)敏感接触点。[【Jan】在此视频中演示触摸点](https://vimeo.com/144485025)。用一堆钉子和一些代码就能做的事情太神奇了！

说到代码，[Jan]，我们很想看看在这个美丽的引擎罩下发生了什么。有机会的话，给我们一些图表和代码？