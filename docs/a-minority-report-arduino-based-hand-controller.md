# 少数报道基于 Arduino 的手控器

> 原文：<https://hackaday.com/2017/06/23/a-minority-report-arduino-based-hand-controller/>

电影喜欢展示他们还不能真正制造的技术。例如，即使在《2001:太空奇遇记》(1968 年上映)中，电脑屏幕实际上也是投影电影。他们用来看新闻的平板电脑看起来像是你今天下午可以在百思买买到的东西。[CircuitDigest]看了《钢铁侠》,这启发了他，想看看他是否能像在那部电影和许多其他电影(包括《少数派报告》)中一样，通过手势控制自己的电脑。虽然他称之为“虚拟现实”，但我们认为 VR 是沉浸在视觉中的，这实际上只是手套，但它仍然很酷。

该项目在手套上使用 Arduino，并在 PC 上进行处理。电脑有一个网络摄像头，可以跟踪手部动作，手套有两个霍尔效应传感器，可以模拟鼠标点击。蓝牙连接手套和电脑。你可以在下面看到一段视频。

该系统需要校准，您可以向其显示您想要跟踪的对象(演示中的亮蓝色圆盘)。该对象显然需要与相机视野中的其他对象具有不同的颜色。这也意味着物体必须留在视野中，所以不要忘乎所以地想着用旋转的手掌做出疯狂的手势。

如果你在 Hackaday 上搜索“手势”，你会发现人们已经“用手”做了所有事情，从玩俄罗斯方块到开车的 T2。也有很多不同的技术在使用，从[雷达](https://hackaday.com/2017/01/24/millimeter-wave-radar-tracks-gestures/)到[重新设计的 Leap 控制器](https://hackaday.com/2015/08/22/follow-me-making-servos-track-hand-motion-with-leap/)。

 [https://www.youtube.com/embed/HEOc6Xc5CAs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HEOc6Xc5CAs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

