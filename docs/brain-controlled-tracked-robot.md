# 脑控履带式机器人

> 原文：<https://hackaday.com/2017/01/20/brain-controlled-tracked-robot/>

[Imetomi]发现自己从一架坏了的无人机上抢救了一台相机，当他决定在一个新项目中使用它时，这是一个带有来自安装的相机的实时视频馈送的履带式机器人。

> …我有一架坏了的廉价中国无人机，但它的摄像头似乎还在工作，当我拆开我的无人机时，我发现了一个带视频发射器的小 WiFi 芯片。我(决定)我将在一个项目中使用这个小电路，我开始购买和回收零件。

作为一个履带式机器人，它可以通过大多数类型的地形，并爬上高达 40 度的山坡。它由两个容量为 2600 mAh 的 18650 锂离子电池供电，遥控器基于 HC-12 串行通信模块。你可以用操纵杆控制它，并在虚拟现实眼镜中观看相机的实时流。这很好，但不是全部。

[Imetomi]还使用了一个被黑掉的 Nacomimi 脑波玩具来制作他的机器人的大脑控制版本。脑电波是通过放置在头皮上的传感器来检测的。为了实际控制它，操作者必须集中右手向右移动，集中左手向左移动，眨眼向前移动，再次眨眼停止。还有一个超声波传感器来帮助导航，所以机器人不会撞到东西。这不是很精确，但你可以随时建立操纵杆版本，或者更好的是，使两个控制版本。

 [https://www.youtube.com/embed/DigkYe_53q0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/DigkYe_53q0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们早在 2009 年就报道过 Arduino 大脑计算机接口，我们提出的建议是一个大脑控制的啤酒机器人。但这也很酷。你可以在这里找到[的建造说明](http://www.instructables.com/id/FPV-Virtual-Reality-Arduino-Controlled-Tracked-Rob/?ALLSTEPS)。如果你建造了一个，让我们知道大脑控制是如何为你工作的。

[via [arduino.cc](https://blog.arduino.cc/2017/01/16/control-a-tracked-robot-with-your-mind-or-joystick/)