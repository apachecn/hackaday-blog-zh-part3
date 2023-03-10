# 倾听手势

> 原文：<https://hackaday.com/2017/11/01/listening-for-hand-gestures/>

想要用手势控制一个 VLC 玩家。他求助于[两个普通的超声波传感器和 Python 来完成这项工作](https://circuitdigest.com/microcontroller-projects/control-your-computer-with-hand-gestures)。当然，还有一个 Arduino。你可以在下面看到结果的视频。

Arduino 代码从两个传感器读取距离，一个用于左手，另一个用于右手。这使得设备能够对靠近或远离一个传感器的单手手势以及双手手势做出反应。例如，抬起你的左手，将它移近或移远，就可以调节音量。右手控制倒带和快进。举起双手将开始或停止播放。

当然，由于 Arduino 正在读取手势，您可以根据自己的需要进行更改。我们可能会将传感器安装在更靠后的位置(或者，可能会增加更多的传感器)，这样你就可以使用三角学来三角测量手的确切位置。嗯，也许不确切，但是你可以了解手从右到左以及向前和向后的运动。

在主机端，Python 接收来自 Arduino 的串行数据，然后模拟击键以获得想要的结果。当然，这也是高度可定制的。

巧合的是，几年前我们做了一个类似的项目，使用一个传感器和 Arduino 看起来像 USB 键盘的能力。我们还看到了 8 个传感器[制作钢琴曲](https://hackaday.com/2017/04/22/ultrasonic-raspberry-pi-piano/)。

 [https://www.youtube.com/embed/sC5FNQU71gA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/sC5FNQU71gA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

