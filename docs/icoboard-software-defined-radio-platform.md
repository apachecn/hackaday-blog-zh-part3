# Icoboard 软件定义无线电平台

> 原文：<https://hackaday.com/2018/03/20/icoboard-software-defined-radio-platform/>

Icoboard 是 Raspberry Pi 的一个插件，板载一个 Lattice iCE FPGA。结合廉价的 A/D 转换器，[OpenTechLab]使用所有开源工具构建了[一个软件定义的无线电。他找到了一些便宜的转换器，价格约为 25 美元，速度足够快(32 MHz)，适合手头的目的。电路板上还有一个数模转换器，他可以找到数据手册。你可以在下面看到一个包含整个项目的视频。](https://opentechlab.org.uk/videos:014:notes)

顺便说一句，这个视频相当长(约一小时),涉及如何创建一个 PC 板来连接 Icoboard 和转换器。还有一个 3D 打印的框架，也有详细的解释。

有一件事还没有涉及，那就是利用硬件实现软件定义无线电。测试设置从一个转换器的输入端获取一个信号，将其馈入 FPGA，FPGA 通过数模转换器将其模拟回来。这是可行的，所以正如他们所说，剩下的只是细节。

我们确信[OpenTechLab]会有更多的视频开始使用这个平台。如果您需要，之前有两个视频介绍了如何设置 Icoboard。当然，我们已经谈了很多 iCE FPGAs。你可能想阅读我们的基础教程来开始。之后，你可以学习如何用这个设备把[变成一个 PWM 发生器](https://hackaday.com/2015/12/16/taking-the-pulse-width-modulation-of-an-fpga/)。

 [https://www.youtube.com/embed/seHwp0WN1oU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/seHwp0WN1oU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

