# 重新思考 3D 打印机的自动底座调平

> 原文：<https://hackaday.com/2016/02/22/rethinking-automated-bed-leveling-for-3d-printers/>

自动调平是所有商用细丝打印机的下一个杀手锏。这个问题已经解决了几十次了。你有太多的方法去做这件事。Printrbot 使用感应传感器来确定金属床相对于喷嘴的位置。Lulzbot Mini 将喷嘴本身接触床角上的四个触点。甚至有一些项目会在凸轮和弹簧系统的帮助下机械调平床。这是一个难题，这些解决方案都不是完美的。[mjrice]一直在思考这个问题，他想到了一个简单、优雅、可以在 3D 打印机上复制的解决方案。这是 3D 打印的 RepRap 解决方案，而且看起来很酷。

mjrice 没有使用喷嘴作为触点，没有使用感应传感器，也没有制造一个由齿轮和凸轮组成的巴洛克式系统，而是用一种老式的方法来做这件事:一个简单的微动开关，与任何 RepRap 的限位开关类型相同。在与喷嘴相同的 Z 位置安装一个开关是一个不确定的想法，因此[mjrice]在打印过程中让这个开关缩回到挤出机中，而不使用任何电机、伺服系统或其他机电发明。

这个装置的关键是一个简单的弹簧和一个齿条。当这个齿条从左侧受到撞击时，它会移动一只手臂，并将开关放在床上。从右侧敲击支架，开关折叠到挤出机中。将这个与打印开始时的一点 g 代码结合起来，开关将向下移动，计算出床的实际高度，并向上翻转。漂亮、优雅，并且用于平台调平的算法已经在大多数主要的打印机固件中。

你可以看看下面这个机制的视频。这是一个很棒的小设备，因为它首先被重新包装，所以它不会出现在专有的 3D 打印机中。

 [https://www.youtube.com/embed/GoCQFhDL5eE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/GoCQFhDL5eE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

