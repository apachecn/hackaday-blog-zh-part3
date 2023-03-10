# Hackaday 奖参赛作品:又一个无人驾驶车辆控制器

> 原文：<https://hackaday.com/2017/06/17/hackaday-prize-entry-yet-another-unmanned-vehicle-controller/>

要制造任何种类的自动驾驶汽车，你都需要一个控制器。它必须处理各种工作——读取传感器输出，控制电机和执行器，管理电源——控制一辆即使是中等复杂程度的车辆也需要大量资源。现代汽车就是一个很好的例子——即使是非自动驾驶汽车也可以有单独的计算机来控制发动机、内部电子设备和安全系统。在这种情况下，[[e . n . Hering]正在开发一种模块化的自动驾驶汽车控制器，称为 YAUVC。](https://hackaday.io/project/11724-yauvc-yet-another-unmanned-vehicle-controller)

首字母缩写代表另一种无人驾驶车辆控制器，尽管它的原名“复仇之飞”并非没有魅力。该项目是围绕模块化和冗余的概念构建的。该控制器主要为飞行器设计，以 ATMega328P 作为主处理器，可以插入各种模块来处理不同的任务。

这种设计选择有几个好处——在实时系统中，用单独的处理器处理单独的任务是有意义的。你很难希望你的四轴飞行器坠毁，因为电池管理程序正在从飞行动力学计算中窃取 CPU 时间。相反，通过将任务卸载到单独的模块，每个模块都可以运行而不会干扰其他模块。然而，模块化也有缺点——保持模块间有效通信的问题就是其中之一。[Hering]还计划确保该系统可以设置为使用多个相同的模块进行冗余——类似于客机上的现代飞行系统，这些系统权衡几台计算机的结果来做出决定。

很多工作已经完成 YAUVC 平台已经充实了主干设计以及 WiFi、加速度计和 GPS 导航模块。我们期待着看到 YAUVC 很快达到飞行就绪状态！

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)