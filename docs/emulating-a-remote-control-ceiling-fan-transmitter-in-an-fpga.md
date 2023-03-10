# 在 FPGA 中仿真遥控吊扇发射器

> 原文：<https://hackaday.com/2016/07/04/emulating-a-remote-control-ceiling-fan-transmitter-in-an-fpga/>

[乔尔]有一个遥控吊扇。这没什么特别的，控制器有一个低功率 350MHz 发射机和一个 Holtek 编码器，通过键入发射机的输出来发送命令。为了得到更好的东西，他开始对设备的协议进行逆向工程，并在点阵 iCE40 FPGA 上实现。

为了解码设备的数据包，他伸手拿起他的 RTL-SDR 接收器，用软件查看了一下。GQRX 确认了携带者的存在，并允许他记录一个原始的 I/Q 文件，然后他可以将该文件提供给 [Inspectrum](https://github.com/miek/inspectrum) 来分析数据包结构。他发现这是一种简单的开关键控方案，通过不同的脉冲宽度来表示比特。然后他能够创建一个 [Gnu Radio](http://gnuradio.org/) 项目来实时读取和解码它们。

当时，仿真发射机是一个相当简单的过程，即利用片上 PLL 产生 350MHz 时钟，并用自己产生的数据流选通该时钟以提供调制。结果，他可以用一根短线天线控制他的风扇，事实上，他担心他公寓里的其他类似风扇也可能会这样。如果你想尝试类似的东西，你可以在 GitHub 上看看他的源代码。

值得指出的是，像这样的发射机会辐射大量基频倍数的谐波，因此输出端没有滤波器可能会造成干扰。尽管它的功率很低，但它也将打破你居住的地方的频谱调节器所设定的所有规则。然而，这是一个有趣的项目阅读，其逆向工程和有点新颖的 FPGA 的使用。

无线远程黑客似乎是黑客社区中最受欢迎的消遣。我们已经有了 [2.4GHz 黑客](http://hackaday.com/2015/09/20/hacking-2-4ghz-radio-control/)和大量[无线电源插座黑客](http://hackaday.com/2014/03/10/hacking-radio-controlled-outlets/)。