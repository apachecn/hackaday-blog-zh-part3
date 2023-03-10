# 斩波器和斩波器稳定放大器是什么？

> 原文：<https://hackaday.com/2018/02/27/chopper-and-chopper-stabilised-amplifiers-what-are-they-all-about-then/>

作为一名刚毕业的工程师，我的第一份工作是维护一套模拟图表记录器。到 20 世纪 90 年代初，它们已经成为了博物馆的展品:一卷电动绘图纸，一支笔可以根据输入端的电压成比例地在上面移动。内部是一个简单的伺服系统，一个差分放大器通过一个电位计比较来自机械装置的反馈和放大的输入。

这些录音机可以追溯到 20 世纪 60 年代初，内部的电子设备来自锗晶体管时代:许多 Mullard OC 系列设备，带有红点的黑漆玻璃管，以及意想不到的，一个连接到 50 赫兹交流电源的大电磁铁，中间有一个簧片开关，这对一个过于自信的年轻人来说是全新的，他认为自己什么都知道。

我偶然发现的是一个斩波放大器，这是一个稍显笨拙且长期被取代的解决 DC 放大问题的方案，在无处不在的集成电路运算放大器出现之前。我们已经如此习惯于 DC 放大器，以至于*只能工作*，以至于我们忘记了曾经有一段时间这种设备是不可能的。同一晶片上的器件之间的属性紧密匹配，使得集成电路运算放大器能够实现稳定的 DC 放大，这种方式使得在具有分立晶体管的相同电路中的最佳尝试都失败了，但在这种情况发生之前，需要采取一些绝望的措施。

[![The classic chopper amplifier. From Analog Devices, MT-055 tutorial.](img/75522dd24698a43adcf93e90c5ecc031.png)](https://hackaday.com/wp-content/uploads/2018/01/ad-classic-chopper-amp1.jpg)

The classic chopper amplifier. From Analog Devices, [MT-055 tutorial](http://www.analog.com/media/en/training-seminars/tutorials/MT-055.pdf).

斩波放大器依赖于一个简单的前提，即使用 20 世纪 50 年代的技术，很难制造一个好的直流放大器，但很容易制造一个好的交流放大器。因此，DC 输入信号被调制到交流电源上，通过交流放大器馈送，然后被解调并通过低通滤波器以恢复放大的 DC 信号。在我的图表记录器中，调制和解调由 50 Hz 簧片开关执行，锗晶体管交流放大器能够很好地处理产生的 50 Hz 方波。

斩波放大器在仪器仪表和其它应用中很常见，直到 20 世纪 60 年代出现价格合理的集成电路运算放大器。当这些元件到来时，它们提供了一个差分放大器，而不是斩波的单端放大器，具有更好的增益和更高的带宽，而价格只是其一小部分，并且没有任何复杂性。你可能会认为这种发展会让直升机成为历史，但事实并非如此！集成电路运算放大器是一种用途极其广泛的器件，可以有许多不同的变体来适应各种各样的应用，但它有一个致命的弱点。很难在几分之一赫兹，即近 DC 频率下制造出低噪声水平的运算放大器。

[![A chopper-stabilised amplifier, from the Texas Instruments App note: Auto-zero amplifiers ease the design of high-precision circuits](img/14354d6c004db9124b456d051feda97d.png)](https://hackaday.com/wp-content/uploads/2018/01/ti-chopper-stabilised-amp.jpg)

A chopper-stabilised amplifier, from the Texas Instruments app note: [Auto-zero amplifiers ease the design of high-precision circuits](http://www.ti.com/lit/an/slyt204/slyt204.pdf).

运算放大器 DC 噪声性能差的问题的解决方案来自于斩波器的回归，但只是作为运算放大器的一个附件，而不是它的替代品。斩波稳定运算放大器是一种标准运算放大器，配置为交流放大器，在其同相输入端的路径上有一个传统的斩波放大器(图中标为“稳定放大器”)。这就变成了一个双路径器件，高频成分由带宽出色的运算放大器放大，而 DC 成分由斩波放大器放大，运算放大器只是一个缓冲器。整个电路仍然是单端的，但它已经成为一个具有超低噪声 DC 性能的高带宽放大器。

![A basic auto-zero amplifier, from Maxim Integrated app note 4179.](img/f06d6c2a72942e0a45348e8461d62a9a.png)

A basic auto-zero amplifier, from [Maxim Integrated app note 4179](https://pdfserv.maximintegrated.com/en/an/AN4179.pdf).

斩波放大器还有最后一项改进，可以从多家制造商那里买到。自稳零放大器使用斩波放大器和运算放大器，就像斩波稳定放大器一样，只是斩波器不直接影响输出。相反，它形成一对采样保持放大器，交替调整自己作为差分放大器的失调，然后调整进行放大的另一个运算放大器的失调。这样可以像简单的斩波放大器一样降低运算放大器的 DC 噪声，同时保留运算放大器的差分输入。

阅读这篇文章的人不太可能会以与老式图表记录器打交道为生，尽管黑客读者从未停止让我们感到惊讶。因此，如果您遇到斩波放大器，它很可能是最后一种，一种自稳零放大器芯片，对您来说可能只是另一种用于应变计或类似器件的运算放大器。但是，即使维护一个 20 世纪 50 年代的振动簧片开关的乐趣不会让你的眉头皱一下，了解一下它们是如何工作的仍然是值得的。如需了解更多信息，我建议您下一步应该访问网上或本页链接的多份应用笔记和数据手册。你的大脑中永远不会储存太多的电路！

图片:老式斩波放大器中使用的机械振动开关。[二元序列【CC BY-SA 4.0】](https://commons.wikimedia.org/wiki/File:Electromechanical_Vibrator.JPG)。