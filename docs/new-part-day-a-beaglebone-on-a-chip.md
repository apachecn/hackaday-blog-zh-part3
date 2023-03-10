# 新零件日:芯片上的比格犬骨

> 原文：<https://hackaday.com/2016/05/10/new-part-day-a-beaglebone-on-a-chip/>

当前的 ARM 单板机有许多共同之处。从 Odroid 到 Raspberry Pi，一切都是围绕片上系统构建的，这是一块硅片，拥有构建最小电路板所需的一切。不过，你不会发现很多硬件黑客在摆弄这些芯片。这需要在电路板上放置一些 RAM 和一些其他高速连接器。到目前为止，制造这些 ARM 板的人只有 Real Engineers，他们的工资与他们的技能相称。

这种情况现在即将改变。Octavo 系统公司推出了一款新产品，该产品或多或少有点像芯片上的小猎犬骨。如果你能把带有 BGA 封装的 PCB 放在烤箱里，你也能构建自己的运行 Linux 的 ARM 单板计算机。

Octavo 的新系统封装是 OSD335x 系列，具有德州仪器 AM335x ARM Cortex A8 CPU、高达 1GB 的 DDR3 和外设，包括 114 个 GPIOs、6 个 UARTs、2 个 SPI、2 个 I2C、2 个千兆以太网和 USB。

商业上可用的单板计算机如 Pi 和 BeagleBone 中使用的芯片有数百个无源元件散布在电路板上。这使得设计这种单板计算机具有挑战性，更不用说实际组装了。Octavo 正在将一堆这样的电阻、电容和电感烘焙到这个芯片中，允许运行 Linux 的极小电路板。[Jason krid ner]——beagle bone 的家伙—[正在开发一款 PocketBone](https://oshpark.com/shared_projects/GWqtFu43) ，这是一款成熟的 Linux 计算机，可以放入 Altoids 罐中。

当然，有了这种程度的集成，芯片上的 BeagleBone 不会便宜。即将发布的该系列的第一个零件号为 AM3358 CPU 和 1GB RAM，[的第一个数量](http://www.digikey.com/product-detail/en/octavo-systems-llc/OSD3358-512M-BAS/1676-1000-ND/6012564)售价为 50 美元。

尽管如此，这是我们从未见过的。这是一台任何人都可以使用的芯片上的 Linux 电脑。该模块有一个老鹰符号。这是一个为硬件黑客设计的芯片，我们迫不及待地想看看使用这种芯片的人会拿出什么。