# 宝丰手持有声电影与 GNU 电台相遇

> 原文：<https://hackaday.com/2017/02/11/baofeng-handy-talkie-meets-gnu-radio/>

曾经有一段时间，几乎每个火腿都有一个昂贵的甚高频或超高频收发器在他们的车上或腰带上。开车的时候和朋友聊天真是太棒了。多亏了自动电话补丁，你甚至可以在任何地方打电话。1980 年，手机还不常见，所以在车上打电话肯定会引起注意。

如今，由于像宝丰、京通和 Anytone 这样的公司的大量进口，业余无线电设备并不昂贵。虽然手持收发器更多的是冲动购买，但由于手机的广泛使用，你不会听到太多的聊天和电话。也许这就是为什么(Bastian)买了一台便宜的宝丰收音机，但从未用过。

他当时正在做一个交通灯项目，想在交通灯改变时发送一个射频信号。他意识到宝丰收音机是一种廉价而令人愉快的解决方案。他只需要一种方法让电脑产生一个音频信号给收音机。他的答案是在 GNU Radio 中设计一个 UDP 包到音频流图。GNU 电台然后传送给宝丰。无线电的内置 VOX 功能处理发射切换。你可以在下面看到一个视频演示。

我们没有看到的是，他打算如何在接收端解调信号。当然，你也可以用 GNU Radio 做到这一点。如果你想要更多类似网络的连接，你也可以改变一些业余无线电软件的用途。别忘了，你需要确保你在当地有合适的执照，可以使用你想要的频段。这些无线电通常会在很宽的频率范围内传输，所以要小心。

这是一个很好的例子，说明了除了 SDR 之外，如何使用 GNU radio。例如，我们已经看到它被用来[生成测试模式](https://hackaday.com/2015/11/22/gnu-radio-drives-oscilloscope/)。如果你想尝试 GNU Radio，我们讨论了如何开始使用[没有特殊硬件](https://hackaday.com/2015/11/11/getting-started-with-gnu-radio/)。

 [https://www.youtube.com/embed/Z93ungdCah8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Z93ungdCah8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

