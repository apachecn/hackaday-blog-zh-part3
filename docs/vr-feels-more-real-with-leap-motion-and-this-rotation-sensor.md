# 使用 Leap Motion 和这个旋转传感器，VR 感觉更真实

> 原文：<https://hackaday.com/2016/11/04/vr-feels-more-real-with-leap-motion-and-this-rotation-sensor/>

在过去几十年的任何时候，你都可以这么说:虚拟现实外围设备的世界似乎还没有发挥出它的潜力。从 Amiga 驱动的虚拟耳机和 20 世纪 90 年代令人恶心的任天堂虚拟男孩到今天的高级耳机和外设，总有一种我们还没有完全到达那里的感觉。随着最新产品的出现，硬件的缺点侵入虚拟世界的情况可能会减少，但虚拟世界沉浸感的目标有时似乎仍然难以实现。

今天市场上更有趣的外设之一是 Leap Motion 控制器。这是一个 USB 设备，包含红外照明和摄像头，为其软件提供足够的分辨率，以准确计算用户手和手指在三维空间中的位置。这种跟踪手指运动的能力使它具有控制器的功能，可以与虚拟世界中的对象进行非常复杂的交互和操作。

即使是跳跃运动也有它的缺点，它无法跟踪的时刻。旋转你的手，例如当你瞄准游戏中的虚拟武器时，会使它变得混乱。这导致[Florian Maurer]寻找自己的解决方案，他想出了[一种包含旋转传感器](http://flrnmrr.com/2016/10/18/wireless-vr-glove-minimalist-controller)的手持外设。

受电影《安德的游戏》中的一个电影道具的启发，这是一个 3D 打印的设备，可以夹在拇指和食指之间的手掌上。它包含一个 Arduino Pro Micro 和一个 bno055 旋转传感器，以及几个用于游戏内操作的按钮，如触发器。它解决了 Leap Motion 的旋转检测问题，并且不会妨碍手的运动，以至于他戴着它也不能使用键盘和鼠标。遗憾的是，他似乎还没有发布任何代码，但他确实向我们展示了一个视频演示，我们已经在休息时发布了这个视频。

 [https://www.youtube.com/embed/3DJi9pYPH4E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3DJi9pYPH4E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



Leap Motion 是一款吸引了许多普通读者想象力的设备。我们已经看到一个[控制一个六足步行机](http://hackaday.com/2013/08/06/leap-motion-controls-hexapod-with-hand-signals/)，也许让·米歇尔·雅尔可以为[找到这个空气竖琴](http://hackaday.com/2012/12/05/air-harp-using-the-leap-motion/)的用途，万一他的激光发生故障的话。