# 使用 3D 打印和 PIC 对电阻器进行分类

> 原文：<https://hackaday.com/2016/12/30/sorting-resistors-with-3d-printing-and-a-pic/>

如果你还没有老到记得在穿孔卡片上编写 FORTRAN 程序，你可能会惊讶于一张标准卡片有 80 个字符，而 FORTRAN 程序每张卡片只用了 72 个字符。原因很简单:keypunches 可以自动在最后 8 个字符中加入一个序列号。你为什么在乎？如果你在走过广场时掉了一盒卡片，你可以用一台机器对最后 8 个字符进行分类，然后把这副牌按正确的顺序放回去。

如今，这不是一个真正的问题。然而，我们弄洒了其中一个小零件箱——你知道有小托盘的那种。我们不太可能再次分离电阻。相反，当我们需要的时候，我们会去寻找我们想要的价值。

[布莱恩·格罗斯]、[内森·兰伯特]和[亚历克斯·帕克赫斯特]更勤奋一些。在康奈尔大学布鲁斯·兰德班级的最后一个项目中，他们制作了一台 3D 打印电阻分拣机。PIC 处理器从料斗中输送电阻器，对其进行测量，并根据其值将其放入正确的容器中。谁不想这样呢？你可以在下面看到一个视频演示。

起初，该设备似乎使用旋转编码器作为输入设备。然而，它不是一个编码器。这是一个 10 圈电位计。这很容易阅读，但会导致一些独特的处理。例如，为了导航 LCD，PIC 查看 pot 值的变化率。然而，如果它看到锅移动到行程的末端，它将导航完全向那个方向移动。

我们认为将它与 [OpenCV 电阻读取器](http://hackaday.com/2015/05/14/reading-resistors-with-opencv/)结合起来会很酷，也可以识别不合规格或标记错误的电阻。实际上[有一些手机应用](http://hackaday.com/2015/09/12/resistance-is-theres-an-augmented-reality-app-for-that/)可以做到这一点，并取得不同程度的成功。

感谢[Bruce]的提示，以及启动这么多年轻工程师。

 [https://www.youtube.com/embed/l50SH11y12c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/l50SH11y12c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

