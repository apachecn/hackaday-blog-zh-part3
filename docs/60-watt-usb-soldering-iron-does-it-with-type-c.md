# 60 瓦的 USB 烙铁使用 C 型烙铁

> 原文：<https://hackaday.com/2017/02/24/60-watt-usb-soldering-iron-does-it-with-type-c/>

前一段时间，我们发表了一篇关于那些便宜的 USB 烙铁的帖子，考虑到它们确实功率不足，这些烙铁看起来惊人地强大。但是 USB Type-C 将会改变这一点。虽然它已经存在了一段时间，但我们现在才开始看到支持 USB-C 的设备和充电器获得牵引力。具有 USB-PD 选项(用于供电)的 USB-C 充电器可以作为高电源，允许对笔记本电脑、电话和其他设备进行快速充电，这些设备能够协商其能够获得的更高电流和电压。[Julien Goodwin]向我们展示了他是如何制造出一个 [USB-C 供电的烙铁，它不会吸东西](http://laptop006.livejournal.com/59591.html)。

他能够以 20 伏和 3 安培的电压驱动普通的 Hakko 熨斗，从 USB-C 充电器为其提供 60 瓦的输入功率。Hakko 的额定工作电压为 24 V，因此其运行电压比~~电源~~低 16%。但即便如此，60 W 对大多数情况来说也足够了。在特殊情况下，USB-C 规格允许最高 5 A 的电流输出，因此使用此功能时几乎有 100 W 可用。

这一切都是从他试图为他的各种计算机整合他的电源砖收集，以减少插头的许多类型和配置开始的。环顾四周，他偶然发现了 [USB-PD 协议](https://en.wikipedia.org/wiki/USB#Power_Delivery_.28PD.29)。在做了功课之后，他决定基于 [TI TPS65986](http://www.ti.com/product/TPS65986) 芯片构建一个具有 PD 功能的 [USB Type-C 充电器板](http://laptop006.livejournal.com/59323.html)，这是一个非常强大的 USB Type-C 和 USB PD 控制器和电源开关。TI 芯片是一个 BGA 封装，所以他不得不外包电路板组装，加上日常工作不断妨碍，他花了相当多的时间才最终测试出来。幸运的是，没有魔法烟雾从电路板上逸出，第一次运行时完美无缺。这是他今年早些时候在 Linux . conf . au 2017 Open Hardware Miniconf 上展示的关于 [USB-C & USB-PD](https://dl.dropboxusercontent.com/u/3239420/USB-C%20%26%20USB-PD.pdf) [PDF]的幻灯片。它对这一标准提供了很好的见解，包括查看他的驱动板原理图。

作为这样一个多功能的系统，我们很可能会看到 USB-C 在未来被用于更多的设备。这意味着我们应该很快就会看到高功率 USB 烙铁出现。但目前，USB-C 和高通的竞争性“快速充电”(QC)技术之间有一场“权力”之争。这有点像 VHS 和 Betamax，这次我们希望更好的技术能够胜出。