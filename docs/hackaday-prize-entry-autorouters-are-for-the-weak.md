# 黑客日奖参赛作品:自动路由器是为弱者准备的

> 原文：<https://hackaday.com/2016/08/11/hackaday-prize-entry-autorouters-are-for-the-weak/>

[Yann]放弃参加今年的 Hackaday 奖对大多数人来说不是很有用。这是一个连接到 16 位并行总线的微型模块，在几个 led 上显示十六进制数。如果你在 1982 年的电脑上诊断一个问题，这是有用的，但只是勉强。这里真正令人惊奇的是[Yann]是如何使用一些奇怪的技术和奇怪的部件廉价而容易地做到这一点的。

这个微型设备的显示器是 36 个发光二极管的阵列，排列成一组五个七段显示器。家酿七段显示器很酷，但他是如何驾驶的呢？肯定不是用微控制器。相反，[Yann]正在使用一个老技巧，使用并行存储器来存储七段显示器的模式。这种并行存储器采用 2 兆闪存芯片的形式，数据输入连接到板上的 16 位输入，数据输出直接连接到 led。这是一个蛮力的方法，但它是有效的。

这个小电路板还有一些附加功能，包括一个以十六进制或十进制、有符号或无符号显示 16 位总线的开关，以及一个改变 led 亮度的电位计。最令人惊讶的部分是[Yann]如何设法将所有这些安装在一个非常非常小的 PCB 上。这主要是因为闪存采用了薄而小的 TSSOP 封装，但将该电路安装到两层电路板上是一项了不起的工作，也是获得 Hackaday 奖的绝佳机会。

The [HackadayPrize2016](https://hackaday.io/prize) is Sponsored by:[![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](https://hackaday.io/atmel) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://www.digikey.com/) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/)