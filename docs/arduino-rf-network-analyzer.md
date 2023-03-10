# Arduino 射频网络分析仪

> 原文：<https://hackaday.com/2016/03/06/arduino-rf-network-analyzer/>

将直接数字频率合成(DDS)芯片、功率检波器和 Arduino 结合在一起，您会得到什么？[Brett Killion]确实做到了这一点，并最终得到了一个实用的网络分析器。

该项目使用 ADI 公司的 AD9851 DDS 芯片，时钟频率为 180 MHz，可输出 0 Hz 至 72 MHz 范围内任意频率的正弦波。巴特沃兹低通滤波器处理 DDS 信号，然后馈入一个双晶体管放大器。该电路将输出约 0dBm 到 50 欧姆。功率检波器是 ADI 公司的 AD8307，带有 50ω输入负载。功率检波器没有滤波，因此可以测量从极低频率到 500MHz 的频率。

[Brett]使用 Python 程序处理来自 Arduino 的数据。例如，这是软件中一个 10 MHz 晶振的曲线图:

[![net10](img/03180e4e59762fca1417a1446bed8d9a.png)](https://hackaday.com/wp-content/uploads/2016/03/net10.png)

如果你想了解更多关于 DDS 的信息，我们自己的【Bil Herd】[已经覆盖了](http://hackaday.com/2014/11/24/direct-digital-synthesis-dds-explained-by-bil-herd/)(见下面的视频)。我们也看到了类似的[天线分析仪](http://hackaday.com/2015/08/06/40-antenna-analyzer-with-arduino-and-ad9850/)，它们是差不多的东西。

 [https://www.youtube.com/embed/MKiP-4o3cFI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MKiP-4o3cFI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

