# 别针背后:树莓皮是如何获得音频的

> 原文：<https://hackaday.com/2018/07/13/behind-the-pin-how-the-raspberry-pi-gets-its-audio/>

单板计算机为我们作为硬件创造者提供了一场计算方式的革命。我们已经习惯了这样一个世界，在这个世界中，整个微型计算机已经成为一个独立的组件，而不是一个复杂的系统，我们通过它们暴露的接口作为无定形的实体与它们交互。但是，单板计算机上的每个引脚或插座背后都有一些东西，所以在最近的一篇新闻中，我们看了一下 Raspberry Pi 上以太网插孔背后的东西，我们希望通过查看更多引脚和接口来继续这个主题。因此，今天我们将继续讨论树莓派，并从一个简单的目标开始，看看它的音频插孔。

自 2012 年以来，除了 Pi Zero 系列之外，所有主要的 Raspberry Pi 板版本都采用了 3.5 毫米插孔承载线路电平音频。通过 Raspberry Pi 网站可以很容易地访问这些电路[，这些电路也很容易理解，因为所有真正困难的工作都是在 Broadcom 片上系统的芯片中完成的。看看音频电路，我们先回到](https://github.com/raspberrypi/documentation/tree/master/hardware/raspberrypi/schematics)[2012](https://www.raspberrypi.org/app/uploads/2012/04/Raspberry-Pi-Schematics-R1.0.pdf)(PDF)最初的 Pi Model B，因为尽管最近的模型有一些变化，但这保持了电路的本质。

[![The audio circuitry from the first Raspberry Pi.](img/363fd9094a29692bba515ca87544ffa9.png)](https://hackaday.com/wp-content/uploads/2018/06/pi-audio-raspi1-audio-schematic-rethemed.jpg)

The audio circuitry from the first Raspberry Pi.

上面的原理图显示了第一个 Raspberry Pi 的音频电路。左边是来自一对 BCM2385 PWM 线路的输入，右边是音频插孔。中间的部分可能看起来很奇怪，这个电路只使用分立元件。即使它整齐地分为两部分，二极管也可以保护输入免受可能通过插孔进入的有害电压的影响，RC 网络是一个滤波器。最后一部分是有趣的部分，值得更深入的解释。

[![](img/b86d4eda81c5b903eb59f4dd70db9c61.png) ](https://hackaday.com/wp-content/uploads/2018/07/pi-audio-raspi1-audio-filters.jpg) PWM，即脉冲宽度调制，是一种完全数字化的方式，将模拟值表示为一串脉冲，其宽度与所表示的模拟值成比例。它本身不是模拟信号，尽管通过低通滤波器将其转换为模拟信号很简单，该低通滤波器的截止频率是模拟信号的最大频率。如果我们再看一下电路的右侧，我们可以看到，使用顶部电路中右通道的数字，R21 和 C20 构成一个低通滤波器。可以计算 270R 和 33nF 的值，以给出略低于 18kHz 的截止频率，这是音频输出的合理声音值。

接下来的两个元件是高通滤波器 R20 和 C48。这消除了任何可能导致不舒服的隆隆声或损坏扬声器的极低频率。150R 和 10uF 的值可以计算为截止频率约为 100Hz，这也是一个合理的数字。这对滤波器的输出应该是可接受的音频信号，并直接进入 3.5 毫米插孔。

## 更新的 Pi，更好的音频

最近的树莓 Pi 模型在音频部门有一些变化。早期的主板有一个较低的音频水平，他们的频率响应可以更好。新版本的电路增加了一个高速缓冲芯片，以提供更低阻抗的源，并稍微调整了滤波器值。

[![The audio circuitry from the Raspberry Pi 3.](img/e82e3b01e1df7e4146f7683af0be3943.png)](https://hackaday.com/wp-content/uploads/2018/06/pi-audio-raspi3-audio-schematic-rethemed.jpg)

The audio circuitry from the Raspberry Pi 3.

低通滤波器的 220R 和 100nF 现在使其截止频率略高于 7kHz，高通滤波器的 100R 和 47uF 使其截止频率为 33Hz。这两个值听起来都很离谱，毕竟 7kHz 根本算不上高保真。但是，如果把计算出的截止频率想象成一堵砖墙，那就大错特错了。事实上，更好的说法是称为*滚降*频率，此时响应开始下降。这些修改后的值将给出一个圆整的频率响应，仍然允许大量高频通过，并阻止大量低频，但最终结果不会超出音频范围太多。

由于[一些困扰电子工程学生的数学问题](https://en.wikipedia.org/wiki/Nyquist_rate)，低通滤波器的响应应该终止于(至少)正在播放的音频的一半采样频率，以避免结果中不必要的失真。这些值为该数字提供了更好的近似值，从而有助于从较新的 Pi 版本获得质量更好的音频输出。

这是一个看起来足够简单的电路，然而却隐藏着惊人的复杂性。除了 Pi 之外，它还有很多用途，因为无论你在哪里使用来自微控制器或 SoC 的 PWM 音频信号，你都需要复制它的功能。