# 热爱音乐的比格波恩

> 原文：<https://hackaday.com/2017/06/14/music-loving-beagle/>

当多个执行器需要相互协调工作时，机器人控制会变得非常复杂。一个简单的机器人手臂需要依次控制每个关节以达到一个特定的位置。BeagleBone Blue 配备了电机驱动器、传感器输入和无线功能，专为机器人设计。

[Andy]已经准备了一个音乐机器人，叫做 [BeagleBone Blue 电子机械钟琴](http://workshopshed.com/2017/04/beaglebone-blue-music-player/)使用单板计算机。硬件由八个伺服电机组成，每个电机上都附有一个槌棒。电机本身安装在 3D 打印的支架上，允许它们安装在正确的高度。伺服连接到主板进行位置控制，但是，必须使用外部电源为所有电机提供必要的电流。

软件端有程序将音符翻译成伺服位置，并通过 MQTT 和 websockets 连接到 web 浏览器。基本的用户界面很简单，有连接和发送击键的按钮。代码以及 OpenSCAD 设计可以从 [GitHub](https://github.com/Workshopshed/musicController) 下载。查看下面的视频进行演示。

这个项目可以扩展到从互联网上播放音乐的自主机器人。我们想起了[扔石头的钟琴](http://hackaday.com/2017/03/15/mechanical-music-maker-throws-stones/)，它很酷，希望两者都有一些变化。

 [https://www.youtube.com/embed/eYo5Z3isM2A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/eYo5Z3isM2A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

