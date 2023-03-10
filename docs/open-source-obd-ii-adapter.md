# 开源 OBD-II 适配器

> 原文：<https://hackaday.com/2016/03/27/open-source-obd-ii-adapter/>

自 20 世纪 80 年代的“白痴灯”以来，汽车诊断已经取得了长足的进步。由于现代车辆中连接到数据网络的众多传感器，当前版本的车载诊断(OBD)协议提供实时数据和故障诊断。虽然硬件接口现在已经相当标准化，但制造商使用几种不同标准中的一种来编码数据。【Alex Sidorenko】已经构建了一个[开源 OBD-II 适配器](http://www.obddiag.net/allpro.html)，它使用 [ELM327 命令集](https://en.wikipedia.org/wiki/ELM327)提供了一个串行接口，并支持所有 OBD-II 标准。

硬件围绕 LPC1517 Cortex-M3 微处理器构建，可接受多种不同版本。这里有 [PDF 原理图](http://www.obddiag.nimg/allpro/AllPro.pdf)，和一套用于 PCB 布局的 Gerber 文件( [ZIP 存档](http://www.obddiag.net/allpro/allpro-mfgr-data.zip.zip))，如果你想深入了解它的内部。 [MC33660 ISO K 线串行链路接口设备](http://www.mouser.com/ds/2/302/MC33660-783676.pdf)用于提供与微控制器的双向半双工通信接口。还包括 [TJF1051，这是一款高速 CAN 收发器](http://www.nxp.com/documents/data_sheet/TJF1051.pdf)，它在微控制器和 ODB-II 连接器上的物理双线 CAN 线路之间提供接口。适配器板的串行输出通过串行转 USB 适配器连接到计算机。

[软件](https://github.com/ObdDiag-Net/allpro)是用 C++为 LPCXpresso IDE 编写的，LPC xpresso IDE 是一个用于 ARM Cortex-M 处理器的 GNU 工具链，但也可以使用其他工具链进行编译。如果你想从源代码构建[固件，或者如果你想通过 Flash Magic](http://www.obddiag.net/allpro_develop.html) 对适配器进行[编程，他会给你指示。](http://www.obddiag.net/allpro_prog.html)

早在 2007 年，我们就推出了[Alex]的基于廉价 PIC 的 ODB-II 接口,所以他已经在这方面工作了一段时间，并且对他正在做的事情有很好的把握。