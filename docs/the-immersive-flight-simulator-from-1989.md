# 1989 年的沉浸式飞行模拟器

> 原文：<https://hackaday.com/2017/06/19/the-immersive-flight-simulator-from-1989/>

个人电脑游戏的历史将拥有当今最先进图形的游戏，如 3D 版 Wolfenstein 和 3D 版 *Doom* 沐浴在荣誉之中。经常被忽视的是*微软飞行模拟器*和更早的，来自 subLOGIC 的前微软版本，包括 1977 年的 Apple II 版本。[Wayne Piekarski]最近在玩 MS 飞行模拟器 4，希望它更像他基于 X-Plane 11 的现代飞行模拟。[这意味着多台显示器，结果是惊人的](http://www.tinmith.net/wayne/blog/2017/06/immersive-flight-sim-4.htm)。

MS Flight Sim 4 的视频和网络功能虽然在 80 年代末令人印象深刻，但仍然非常有限。在 1989 年，计算机只支持单个显示器，而 FS4 有能力将机器联网在一起进行空战，但没有办法将摄像机视点设置到远程飞机上。

这个问题的解决方案以内存转储的形式出现。由于[Wayne]在 DOSBox 中运行 FS4，他能够读取游戏的一个实例的内存，并将这些内存位置写入游戏的另一个实例。DOSBox 实例中只有 18 字节的内存，包括模拟飞机的航向、高度、横滚和俯仰信息。[Wayne]正在将这些数据发送到 FS4 的其他实例——有效地在另一台机器上镜像游戏——并更改相机视图以查看左右窗口。他在额外的监视器上显示这些视图，然后就完成了。

结果正是你所期望的。[Wayne]现在从梅格斯机场起飞，在芝加哥市中心的 10 或 12 栋建筑中嗡嗡作响，并拥有 180°全景。看看下面的视频。

 [https://www.youtube.com/embed/hbwnvPLpLos?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hbwnvPLpLos?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent) 
 [https://www.youtube.com/embed/ppzBk8IUp58?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ppzBk8IUp58?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

