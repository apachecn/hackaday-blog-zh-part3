# Hackaday 奖参赛作品:蝎子 DC-DC 电压转换器

> 原文：<https://hackaday.com/2017/10/04/hackaday-prize-entry-scorpion-dc-dc-voltage-converter/>

对于你我来说，找到合适的壁灯或充电器可能是一件很方便的事情，但有些人真的真的需要合适的充电器，因为没有它可能意味着火灾。

[marius]是一名罗马尼亚硬件工程师，他搬到了巴布亚新几内亚，在那里他有机会在该国的偏远丛林中旅行。在那里，他看到许多人使用太阳能电池板在晚上为 3W 灯泡的汽车电池、他们的手机或其他每天只需要几瓦时的便利设施充电。将汽车电池直接连接到太阳能电池板并不是一个明智的想法，所以[marius]着手创造一种简单、成本非常低的 DC-DC 电压转换器。他称之为 Scorpion 3.0(T1)，对于远离电网的低收入地区来说，它看起来是一个神奇的工具。

Scorpion 的设计由一个 3D 打印外壳组成，一个分叉端包含一些鳄鱼夹导线，另一个是标准的桶形插孔。中间是显示输入和输出电压的字符显示器，以及用于用户交互的简单旋转编码器。Scorpion 3.0 的电路主要由一个廉价的低功耗 MSP430 微控制器组成，该微控制器管理显示器、编码器和降压转换器。

为脱离电网的用途设计一些东西意味着一些工程上的挑战，而且在新几内亚的波帕，还有一些环境方面的考虑。[马里乌斯]正在给他的 3D 照片上漆。不，它的防护等级不会达到 IP68，但还是有帮助的。使蝎子便宜也是一个大的考虑，最有可能导致 MSP430 的选择。

这是一个伟大的项目，也是进入 Hackaday 奖的绝佳机会。你可以看看下面蝎子的演示视频。

 [https://www.youtube.com/embed/0v20HoM4c-A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/0v20HoM4c-A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)