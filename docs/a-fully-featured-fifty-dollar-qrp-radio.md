# 一台功能齐全的五十美元 QRP 收音机

> 原文：<https://hackaday.com/2017/09/13/a-fully-featured-fifty-dollar-qrp-radio/>

QRP 无线电运营商试图用最小的功率获得最大的覆盖范围。这个术语来自 QRP Q 代码，意思是“降低功率”多年来，人们为此制造了一些成本非常低的收音机。也许最著名的 QRP 套装是 Pixie，它在易贝售价不到 3 美元。

QCX 是 QRP 实验室的一个新的 DIY QRP 收音机套件。不像 Pixie，它有一长串的功能。QCX 工作在 80、60、40、30、20 或 17 米波段，输出功率高达 5W。显示器提供调谐信息、S 表和 CW 解码器。板载微动开关的功能相当于一个基本的莫尔斯键，也支持外部抑扬或直键。可选的 GPS 可用作频率参考。

该无线电基于 Silicon Labs [Si5351A 时钟发生器](https://www.silabs.com/products/timing/clocks/cmos-clock-generators/device.si5351a-b-gt)，这是一个 PLL 芯片，具有从 2.5 kHz 到 200 MHz 的三个时钟输出。该系统由 Atmel ATmega328P 控制。

对该工具包的需求一直很高，不幸的是，你将不得不等待一个。然而，你可以放下你的 49 美元，在等待发货的时候学习莫尔斯电码。虽然该项目似乎不是开源的，但[汇编指令](http://qrp-labs.cimg/qcx/assembly_A4.pdf)【PDF 警告】提供了完整的原理图。