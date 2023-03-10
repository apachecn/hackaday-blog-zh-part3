# 演讲者制作了一台激光扫描显微镜

> 原文：<https://hackaday.com/2017/02/15/speakers-make-a-laser-scanning-microscope/>

最近我们看到人们对 LSM(激光扫描显微镜)很感兴趣。[Stoppi71]使用一个 Arduino，一个 CD 驱动器，以及最重要的是，他的产品中有两个扬声器。扬声器用于少量移动样品。

扬声器根据通过数模转换器输入的电压在 X 轴和 Y 轴上产生运动。[Stoppi71]声称这项技术可以产生微米范围的运动。他的结果似乎证明了这一点。你可以在下面看到一段关于这款设备的视频。

奇怪的是，[Stoppi71]发现旧的 CD 驱动器更容易操作，因为它们不像更现代的版本那样小型化。该设备使用 Arduino 来驱动扫描台(扬声器)，并读取光电探测器。扫描结果出现在液晶显示屏上。

[![cal](img/b432e2b950815c08ed6fd6b05a750055.png)](https://hackaday.com/wp-content/uploads/2017/02/cal.jpg)【stoppi 71】使用来自易贝的校准载玻片，为不同的放大倍率校准设备。你可以看到中等放大倍数的测试幻灯片。根据记录，一根人类的头发大约有 40 或 50 微米厚。所以照片中 10 微米的标记就像把一根头发分成四分之一或五分之一。

真正的目的是查看光盘上的坑，该仪器完全能够做到这一点。图像不会一下子显示出来(毕竟它是扫描的)，这不是你从光学显微镜中所期望的那种视图，但是典型的光学显微镜不能分辨低于大约 0.2 微米的图像。特殊的技术可以把它压得更低，但是能够用这么简单的东西解决一到两微米的问题是一项伟大的成就。

我们最近看到了一个不同外观的 [LSM，它建立在传统的显微镜载物台](https://hackaday.com/2017/02/08/laser-scanning-microscope/)和 DVD 驱动器上。如果 LSM 对你来说还不够，也许你应该参加一下[开源电子显微镜项目](https://hackaday.com/2016/12/02/nascent-project-open-source-scanning-electron-microscope/)。

 [https://www.youtube.com/embed/du1-rj-ZcM4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/du1-rj-ZcM4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

