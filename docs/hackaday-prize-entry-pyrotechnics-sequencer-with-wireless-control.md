# Hackaday 奖参赛作品:带无线控制的烟火序列器

> 原文：<https://hackaday.com/2017/10/19/hackaday-prize-entry-pyrotechnics-sequencer-with-wireless-control/>

[visualkev]的朋友正在上演他自己的焰火表演，依次点燃每一个，然后跑开。[visualkev]突然想到，他的朋友自己并不真正喜欢这场表演，因为他在躲避，而不是看热闹。另外，这有点危险。因此，他将自己的黑客技能应用于这项挑战，创造了一个定制的烟花序列器。

他使用了来自 OSH Park 的定制 PCB，ATMega328P 控制 8 个 TPIC6C595 8 位移位寄存器，依次触发连接到烟花的 64 个继电器。一个 5V 调节器从 5 节 5AA 电池为项目供电，他用 8 线带状电缆保持电线整洁。

启动序列是一个普通的无线遥控器——沃尔玛的便宜货——让[visualkev]的朋友可以用一只手发射烟花，同时用另一只手操作烧烤钳。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)