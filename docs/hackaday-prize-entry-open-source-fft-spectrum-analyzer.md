# Hackaday 奖参赛作品:开源 FFT 频谱分析仪

> 原文：<https://hackaday.com/2016/07/06/hackaday-prize-entry-open-source-fft-spectrum-analyzer/>

每台机器都有自己与操作者交流的方式。有的发状态邮件，有的发光，但大部分都是震动，发出噪音。如果它高兴地嗡嗡叫，这通常是一个好迹象，但如果它大声抱怨，维修就过期了。[Ariel Quezada]想弄清楚机器振动的意义，并从中得出整体机械状况的结论。他的项目是一款三轴[开源 FFT 频谱分析仪](https://hackaday.io/project/12109-open-source-fft-spectrum-analyzer)，他不仅获得了 2016 年 Hackaday 奖，还进入了竞争激烈的声学缺陷识别领域。

[![open_fft_machine](img/29f9b6110b2e556fa21021173887892d.png)](https://hackaday.com/wp-content/uploads/2016/06/open_fft_machine.jpeg) 在频谱分析仪的硬件方面，【Ariel】为 Arduino Nano 配备了 ADXL335 加速度计，能够拾取 X 轴和 Y 轴上 0 至 1600 Hz 频率范围内的振动。一个薄膜容器，配有便于安装的强磁铁，用作传感器的外壳。[Ariel]编写的固件是一段高效的代码，可以在大约 5000 Hz 的自由运行环路中对来自加速度计的模拟信号进行采样。它通过串行端口将数字化波形传输到主机，在主机上，波形被 Python 脚本捕获并存储，以供进一步处理。

从那里，另一个 Python 脚本过滤捕获的波形，应用窗口函数，计算傅立叶变换，并将频谱绘制成图形。随着分析仪的启动和运行，[Ariel]继续在他可以使用的任意旋转机器的大型轴承上测试该设备。一系列涉及在旋转轴上增加偏心重量的测试表明，分析仪已经能够区分不同等级的不平衡。

The [HackadayPrize2016](http://hackaday.io/prize) is Sponsored by: [![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](http://hackaday.io/atmel)  [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](http://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](http://www.digikey.com/)  [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](http://supplyframe.com/)