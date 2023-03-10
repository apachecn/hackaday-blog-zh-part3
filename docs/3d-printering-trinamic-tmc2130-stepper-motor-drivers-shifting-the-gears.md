# 3D 打印:Trinamic TMC2130 步进电机驱动器

> 原文：<https://hackaday.com/2016/09/30/3d-printering-trinamic-tmc2130-stepper-motor-drivers-shifting-the-gears/>

调整相电流，启动微步，然后忘掉它——这是大多数人对步进电机驱动器 IC 的期望。虽然它们为我们大多数的 CNC 机器和 3D 打印机提供动力，作为“让它旋转”的整体解决方案，我们并不经常关注它们。

在本文中，我将介绍 Trinamic TMC2130 步进电机驱动器，它提供了比您可能需要的更多的功能。一方面，该驱动器可以通过其 SPI 接口进行配置，以适应几乎任何采用步进电机的应用。另一方面，也可以直接写入线圈电流寄存器，将适用范围远远扩展到电机以外。

[![tmc_top](img/9d187ddca2694012f1fb24cdac160618.png)](https://hackaday.com/wp-content/uploads/2016/09/tmc_top.jpg)

The TMC2130 SilentStepStick’s top side with SPI headers and heatsink.

上个月，我们仔细研究了常见步进驱动器 IC 上的微步，但忽略了我们真正想要使用的:智能芯片。Trinamic 提供了市场上一些最智能的步进电机驱动器，自从德国黑客商店 [Watterott](http://www.watterott.com/) 为 TMC2100 和 TMC2130 发布了他们的 [SilentStepStick](https://github.com/watterott/SilentStepStick) 分线板以来，他们也为 DIY 3D 打印机、研磨机和取放机器人设定了新的标准。我最近为我的 Prusa i3 3D 打印机购买了一套这两种产品，带有 SPI 配置接口的 TMC2130 真正引起了我的注意。

不应将 TMC2130 SilentStepStick 与更受欢迎的 — [TMC2100](http://hackaday.com/2015/01/24/new-part-day-silent-stepper-motors/) 变种混淆。顾名思义，它是一个 StepStick 兼容分线板，就像它著名的兄弟一样，在小 PCB 的底部有一个 Trinamic IC。几个过孔和铜溢出物将热量从 IC 的中心焊盘传导出去，允许顶部的散热器有效地冷却驱动器。

[![tmc_bottom](img/bbb794ac093b9aac30bf8c6562898688.png)](https://hackaday.com/wp-content/uploads/2016/09/tmc_bottom.jpg)

The bottom side with the stand-alone mode solder blob jumper next to the IC.

然而，与 TMC2100 不同的是，它不会让你的马达马上旋转起来。你有两个选择:在独立模式下硬连线它，这实际上是把它变成一个 TMC2100，或者连接到它的 SPI 接口，如果你想摇动或搅拌你的步进电机，就拨入。事实上，丰富的配置寄存器使 TMC2130 成为一款非常容易被黑客攻击的芯片，因此我甚至没有考虑在 SilentStepStick 底部桥接一个可以激活独立模式的跳线。

## 第一步

[![](img/badac09418662f893edb57c3cd556f38.png)](https://hackaday.com/wp-content/uploads/2016/09/tmc-wiring-01.jpg)

Wiring the TMC2130 to a classic RAMPS 1.4.

如前所述，在驱动程序执行任何操作之前，它希望进行配置，值得一提的是，所有配置寄存器都是不稳定的，因此，如果我想在我的 3D 打印机中使用它们，我需要将它们配置为打印机启动例程的一部分。

我的 3D 打印机上的[斜坡 1.4](http://www.reprap.org/wiki/RAMPS_1.4) 通过其 [AUX3 引脚头](http://www.reprap.org/wiki/File:Arduinomega1-4connectors.png)以及两个额外的数字引脚(D53 和 D49)断开了底层 Arduino 的硬件 SPI 接口，我用于电缆选择信号。压接电缆将两个 TMC2130 连接到 AUX3 接头后，我可以开始研究软件部分。

Watterott 提供了一个[示例草图](https://github.com/watterott/SilentStepStick/blob/master/software/TMC2130.ino)，它将一个基本配置写入驱动器的寄存器，并旋转一个附加的步进电机。很棒的东西，但是[数据表](http://www.trinamic.com/_articles/products/integrated-circuits/tmc2130/_datasheet/TMC2130_datasheet.pdf)描述了 23 个等待微调的配置寄存器，还有 8 个用来读取诊断和状态数据。所以，我给[写了一个小小的 Arduino 库](https://github.com/makertum/Trinamic_TMC2130)，这将使众多的配置参数以一种更实用的方式可用。从那里，我可以将我的库包含到我正在使用的 Marlin-RC7 3D 打印机固件中。幸运的是，当前的 Marlin 发布候选版本已经支持 TMC26X 驱动程序，所以我可以重用它的一些代码来[组装一个 Marlin fork](https://github.com/makertum/Marlin) ，在其基于 define 的配置文件中包含 TMC2130 的 59 个参数。然后，我可以带着小伙伴们出去兜风。

![tmc_test_setup](img/22ec2531000ddc447e4a3ef215b09639.png)

First steps on a RAMPS 1.4 on a somewhat-uino (sorry Massimo). The testing-contraption to the left is a NEMA 17 stepper motor attached to an encoder.

## 带他们去兜风

随着硬件的设置和软件的正常运行，我运行了一些健全性测试:打开和关闭参数，检查驱动程序的行为在打印过程中如何变化。由于 TMC2130 让您可以调整它正在做的几乎所有事情，这是一个很好的第一步，有助于消除一些变量，并挑选其他值得深入研究的变量。大多数设置可以在运行中和打印过程中更改，但是，在电机运行时，并非所有参数都可以安全地更改。

[![tmc_installed2](img/6235ae23d58d96dc6b40f26a1ec590a2.png)](https://hackaday.com/wp-content/uploads/2016/09/tmc_installed2.jpg)

The TMC’s in service. I’m using the SPI-configurable TMC2130’s (silver heatsink) for the X- and Y- axis. The Z-axis and the extruder feature the TMC2100 (black heatsink). All of them are sitting on additional free-runner diode protection shields.

[![tmc-quick-start-guide](img/4da69d9f4bd13831b8fa790c9c42585f.png)](https://hackaday.com/wp-content/uploads/2016/09/tmc-quick-start-guide.jpg)

An excerpt of Trinamic’s thorough quick start guide.

为了针对特定应用实际调整驱动器，Trinamic 在[数据表](http://www.trinamic.com/_articles/products/integrated-circuits/tmc2130/_datasheet/TMC2130_datasheet.pdf)中提供了快速入门指南，以及关于每个参数及其交互方式的详细信息。基本上，第一步是[通过使用无声棒上的板载电位计调节均方根线圈电流](https://github.com/watterott/SilentStepStick/blob/master/docu/FAQ.md#how-to-set-the-stepper-motor-current)。然后，我们需要选择模拟输入引脚作为电流调整基准，以便实际利用电位计。上面提到的[库](https://github.com/makertum/Trinamic_TMC2130)让我通过一个简单的方法做到这一点:

```
myStepper.set_I_scale_analog(1); // 0: internal, 1: AIN
```

运行电流和保持电流是应该调整的第一个实际参数，运行电流通常为所需的最大电流，保持电流为该值的 70%。静止支架和从运行电流到保持电流的转换之间的延迟可以在 0 到 4 秒之间调整，现在，我将其设置为 4 秒，实际上在 3D 打印机运行时禁用电流减少。这三个值共享一个只写寄存器，因此相应的方法调用如下所示:

```
myStepper.set_IHOLD_IRUN(22,31,5); // [0-31],[0-31],[0-5]
```

并将运行电流设置为 100% (≙ 31)，将保持电流设置为该值的大约 70%(≙22)，并将两者之间的延迟设置为 4 秒(≙ 5)。

我需要扭矩，所以我可以禁用 stealthChop。数据手册建议了一些用于配置斩波器关断时间和比较器空白时间设置的起始值，但由于这是开关噪声和扭矩之间的一个关键权衡，因此迭代其它值也是有意义的。这两个值的库方法如下所示:

```
myStepper.set_tbl(1); // [0-3]
myStepper.set_toff(8); // [0-15]
```

最后，我需要选择一个微步分辨率，并选择是否要使用 256 微步插值功能，本文稍后将对此进行介绍:

```
myStepper.set_mres(32); // {1,2,4,8,16,32,64,128,256}
myStepper.set_intpol(1); // 0: off, 1: interpolate
```

我还没有走过整个调谐程序，其中包括监测线圈电流的范围和消除失真的零交叉，但我得到了驱动器的潜力线索。

## 果汁

它的最大连续均方根电流约为每个线圈 1.2 A(至少在 SilentStepSticks 的 QFN 封装中)，这使它看起来像一个低电流驱动器，不如常见的 A4988 和 DRV8825。实际上，它智能地利用了 2.5 A 的峰值电流裕量，性能优于两者。这为 3D 打印提供了足够的扭矩。不过，我不建议将它们推至 0.9 A RMS 以上，因为如果 IC 需要更多电流，它会瞬间拉高电流。对于 SilentStepStick 用户，这是 0.88 V 的 V [ref] ，通过 SPI 接口，您可以选择当电机旋转和空转时，希望通过电机线圈发送多少电流。当电机处于静止状态时，您可以选择多少秒后开始将电流降低到较低的保持电流，然后降低到更低的空载电流。当然，你也可以将它设置为最大限度地挤出果汁。

## 换挡

开始变得有趣的是像高速模式这样的设置。高于一个可配置的速度阈值，驱动程序会自动将斩波器切换到更快的衰减时间，以挤出一些额外的速度。一旦达到速度，你还可以通过让驱动程序从微步模式切换到全步模式来换档。

## 微步进

选择更精细的微步进分辨率可以平滑步进器的运动，减少振动，有时甚至可以提高定位精度。然而，它也增加了微控制器的负载，每秒钟必须产生 16、32 或 256 倍的步进脉冲。TMC2130 允许您选择 1 至 256 微步/全步进的输入分辨率，然后选择将输出分辨率插值至 256 微步。这使得即使在*越来越落后的* 8 位 AVR 运动控制器上也能平稳运行，这些控制器不能提供高步进频率。此外，通过将 TMC2130 的接口配置为双边沿步进脉冲，您几乎可以零成本地将步进频率至少提高一倍。鉴于现代 IC 仍然具有经典的步进/方向接口，甚至还有一个使能引脚，这些额外的功能实际上使它成为不太新的 CNC 和 3D 打印机电子设备的一个不错的升级。

## 噪声降低

[![tmc-stealth-chop](img/6a2811fc376d3b8efcb5d39278ee6c01.png)](https://hackaday.com/wp-content/uploads/2016/09/tmc-stealth-chop.jpg)

The TMC2130’s datasheet promises undistorted output with stealthChop.

与 TMC2100 一样，TMC2130 具有两种高效、静音的驱动模式:spreadCycle 和 stealthChop。前者以相对较低的噪音排放提供高扭矩，后者几乎听不见，关于这是否会影响扭矩，存在相当多的困惑:一些用户体验到[扭矩](http://toms3d.org/2015/01/05/honest-pre-review-the-all-new-trinamic-tmc2100-stepper-drivers/)大幅降低，而 [Trinamic 关于这个问题的论文](http://www.trinamic.com/_scripts/download.php?file=_articles%2Fproducts%2Fintegrated-circuits%2Ftmc2130%2F_appnotes%2FAN021-stealthChop_Performance_comparison.pdf)陈述了相反的情况。低于 300 RPM(典型的 3D 打印速度)，stealthChop 根本不会影响扭矩。根据 Stephan Watterott 的说法，大多数 3D 打印机固件中使用的双步进和四步进可能是这种情况的原因。

无论哪种方式，灵活的 TMC2130 都允许您自己调整斩波器，以针对您的应用在扭矩、噪声和效率之间找到正确的平衡。在这方面，一个更值得注意的选择是随机选择斩波器的关闭时间。由于大多数可听见的噪音是由于斩波器忙于切换步进电机的线圈而释放出来的，这个选项将噪音分散到更宽的频率范围内，以主观地使步进电机静音。

## 失速检测

TMC2130 通过测量电机的反电动势来检测电机何时失速和失步。在此过程中，它会计算错过的步数，使控制器能够补偿否则不可逆转的失步。这也是一种对障碍物做出反应而不是全力以赴的好方法，当然，该功能可以用作 axis 终点挡板。Trinamic 称这个特性为 [StallGuard](https://www.youtube.com/watch?v=Prw7wNa20Gk) ，就像这个电机驱动器中的其他东西一样，它是高度可配置的。

## 直接方式

[![microstepping_exlained-01](img/c3b7adef64f41d3c7c738570d97655ab.png)](https://hackaday.com/wp-content/uploads/2016/08/microstepping_exlained-01.png) 除了让电机司机为你处理一切，你还可以选择*直接模式*。这种模式实际上将驱动器变成一个带 SPI 接口的双通道、双极性恒流源。你仍然可以用它作为马达驱动器，但可能性远不止于此。值得一提的是，这里的数据手册可能有点混乱，对应的 XDIRECT 寄存器实际上为每个线圈接受两个带符号的 9 位整数(不是 8 位),并在 254(不是 255)的数值范围内正常工作，以改变 I [max/RMS] 之间的电流..

## 外卖

在 Watterott 的分线板发布约半年后，更智能的步进电机驱动器的潜力激起了 3D 打印社区的好奇心，但在实施方面没有太多进展。诚然，让它们运转起来需要一些努力。如果你仍然忙于在 3D 打印机上输入温度，你肯定不想添加几十个新的变量，但如果你热衷于充分利用它，TMC2130 可以提供很多功能:低噪音打印、高速打印、故障时打印中断和从丢失的步骤中恢复。因为驱动 IC 是如此的*可攻击*，它显然是为了适应特定的应用。将其放在通用测试台上可能不会产生有意义的通用结果。

我希望你喜欢看一个比通常更智能的步进电机驱动器，作为 DIY 3D 打印的新前沿之一，以及作为许多其他应用程序的有趣组件。如果你正在考虑在你的 3D 打印机中试验这种 IC 或分线板，请随意尝试我的[马林叉](https://github.com/makertum/Marlin)来开始。如果你正在构建完全不同的东西，底层的 [Arduino 库](https://github.com/makertum/Trinamic_TMC2130)将会帮助你。还有谁在使用这部分？我将很高兴在评论中听到你的想法、应用和经验！