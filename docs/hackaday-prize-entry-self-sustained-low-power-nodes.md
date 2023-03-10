# Hackaday 奖参赛作品:自持低功耗节点

> 原文：<https://hackaday.com/2017/05/15/hackaday-prize-entry-self-sustained-low-power-nodes/>

考虑一下物联网。一个由互联设备、可编程物质和可穿戴电子设备组成的庞大网络只能意味着一件事:将会有大量的电池。虽然更换烟雾探测器的电池似乎可以忍受，但更换 1000 个传感器节点的电池是站不住脚的。这个问题的解决方案是独立的传感器节点，目前移动设备最好的能源可能是太阳能。

为了他的 Hackaday 奖参赛作品，[Shantam Raj] [正在建造一个独立的传感器节点](https://hackaday.io/project/20523-sun-self-sustained-ultralow-power-node)。这是一个用于*互联网*方面的蓝牙设备，但这个设备的真正诀窍是太阳能采集和通过优化固件的低功耗能力。

基本上，这个系统是一个带蓝牙的低功耗 SoC。该设备的电力来自一个小型太阳能电池，再加上一个非常高效的电源和村田公司的一些新的有趣的超级电容器。这些超级电容器体积极小，存储容量高，ESR 低，可快速充电和放电。测试板(见下面的视频)提供了概念验证，但这款设备有一个问题:板上只有一个“健全检查”/电源 LED，消耗 4 mA。运行优化固件时，微控制器的功耗仅为 1 mA。是的，原型中的 LED 仅作为设备开启的指示，是整个系统中最大的功耗。

这个项目很棒，这正是我们在 Hackaday Prize 中寻找的东西。如果物联网真的像预想的那样发生，我们将被埋在堆积如山的纽扣电池锂电池下。某种能量收集计划是解决这个问题的唯一方法，我们很高兴看到有人正在解决这个问题。

 [https://www.youtube.com/embed/p8QcGJfqtu0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/p8QcGJfqtu0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)