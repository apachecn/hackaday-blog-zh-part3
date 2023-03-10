# 精心设计的无线电时钟 Aces 的形式和功能

> 原文：<https://hackaday.com/2017/03/22/well-engineered-radio-clock-aces-form-and-function/>

通过接收到的无线电信号读取时间的时钟比它们的互联网连接、NTP 同步的兄弟有几个优势。无线电信号无处不在，在从发射天线延伸到数千公里的相当大的覆盖范围内都可以获得。这使得这种时钟在没有互联网服务的地区也能可靠地工作。与 GPS 时钟相比，它们的前端电子设备和天线要求要简单得多。[Erik de Ruiter]的 [DCF77 分析仪/时钟](https://create.arduino.cc/projecthub/edr1924/dcf77-analyzer-clock-v2-0-c25404)与德国 DCF77 无线电信号同步，该信号来自 PTB 总部的原子钟。它具有大量的功能，同时仍然易于构建。这是德国黑客工程的一个巧妙之处，让我们惊叹不已。

在时钟功能中，它显示时间、星期几、日期、CET/CEST 模式、闰年指示和星期数。最后一个不是 DCF77 协议的一部分，而是通过软件计算的。DCF77 分析仪拥有从无线电信号中收集的所有有用信息。有时间周期、脉冲宽度、位计数器、位值指示器(0/1)和错误计数器的显示。有两个由 59 个 led 组成的环，每个环提供有关 DCF77 信号的更多信息。前面板上的 PIR 传感器有助于将时钟置于省电模式。最后，还有一大串指示灯和一组开关来控制各种功能。在后面板上，有用于 DCF77 接收器天线板、温度传感器和 FTDI 串行的 RJ45 插座、一组音频声卡控制、复位开关和模式控制开关。

他的构建从外壳的设计和布局开始。在他对结果满意之前，前面板布局必须经过几次迭代。最终版本由铝涂层夹层板制成。他使用在线服务来光刻标记，然后用铣床雕刻出各种窗口和安装孔。后面板是带有激光雕刻的有色丙烯酸树脂，这使得观众可以看到整齐的内部结构。木制框架由 40 年的红木制成，来源于一张古老的传家宝书桌。所有这些努力的结果是一个真正专业的产品。

除了定制的 LED 驱动板之外，电子器件大多是现成的模块。该设备的核心是 Arduino Mega，因为它提供了大量的输出。围绕 [Maxim 7221](https://datasheets.maximintegrated.com/en/ds/MAX7219-MAX7221.pdf) (PDF)串行接口 LED 驱动器有七个 LED 驱动器板——两个用于驱动内环和外环 LED，其他用于各种七段显示器。众多的信号器 led 直接由 Arduino Mega 驱动。他的构建真正融合了噪声弹性 [DCF77 解码器库](https://github.com/udoklein/dcf77)，由【Udo Klein】开发，运行在独立的 Arduino Uno 上。他所有的设计源文件都发布在他的 [GitHub 知识库](https://github.com/deruiter/DCF77-Analyzer-Clock-V2.0)上，他希望能很快发布一个指南，供那些想要自己制作一个的人使用。

在下面的第一个视频中，他展示了时钟的各种功能，在第二个视频中，他向我们展示了时钟的内部。观看，并感到惊讶。

谢谢你的提示，[尼克]

 [https://www.youtube.com/embed/ZadSU_DT-Ks?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZadSU_DT-Ks?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/sP-b0La4Qb4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/sP-b0La4Qb4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

