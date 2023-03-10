# 生物识别手环通电解锁平板电脑

> 原文：<https://hackaday.com/2015/12/08/biometric-bracelet-electrifies-you-to-unlock-your-tablet/>

研究人员[Christian Holz]和[Marius Knaust]提出了一种很酷的新方法，可以在几乎任何触摸屏设备上验证你的身份。这个聪明的想法将生物传感器和低数据速率发射器结合在一个可穿戴的腕带上，通过给 *you* 通电来与触摸屏对话。

具体来说，表带的电极通过手指将 50V、150kHz 的信号耦合到触摸屏。触摸屏通过[普通电容感应方法](https://en.wikipedia.org/wiki/Capacitive_touch_screen)获取你手指的位置，以及“手表”传输的背景信号。这个背景信号被调制开和关，传输你的生物数据。

生物数据本身就是通过你的手腕从一个电极到另一个电极的阻抗。随着多个电极环绕你的手腕，它们最终会像猫一样扫描你手腕的电阻。显然这是独一无二的，足以用作生物识别。(我们很惊讶。)

在我们看来，这种认证技术的最大限制是，由于触摸屏的更新速度相对较慢，因此“手表”每秒只能传输大约 12 位，而触摸屏根本不是为此设计的。假设出于安全原因，您需要一个相当长的密钥，我们担心您会坐在那里，手指在屏幕上停留相当长的时间。不过，研究人员提出了一个很酷的解决方法。他们用心电图电极对屏幕进行了第二次测试，测试了平板电脑的声卡，得到了明显更高的数据速率。(还有蓝牙。)

无论如何，我们认为通过给手指通电来在触摸信号的背景下编码用户数据的想法非常棒。我们看到这个设备有更多的潜在乐趣。例如，你可以玩多人触屏游戏，平板电脑可以告诉你谁在哪里触摸了它。

这里有一个直接链接到他们关于技术的论文。

 [https://www.youtube.com/embed/FgnJee0mVgQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FgnJee0mVgQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

