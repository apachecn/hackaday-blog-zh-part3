# 求助:Rigol 硬件上的开源示波器

> 原文：<https://hackaday.com/2017/04/27/help-wanted-open-source-oscilloscope-on-rigol-hardware/>

我们经常听到(并说)如果你不能破解它，你就不拥有它。我们注意到[tmbinc]已经就他的最新项目发出了求助:为 Rigol DS1054Z 和类似的示波器开发新的固件和 FPGA 配置。它还没有接近完成，但也不是白日梦。[tmbinc]已成功引导 Linux。

不过，还有很多事情要做。他正在通过 JTAG 加载一个引导加载程序，并从 USB 端口引导 Linux。很明显，你想把这些都闪现出来。Linux 让他可以使用 USB 端口、LCD、网络插孔以及前面板 led 和按钮。然而，所有实际的示波器电子器件、FPGA 功能以及处理器和 FPGA 之间的通信都是前向工作。

为什么是里戈尔？[tmbinc]说它们很便宜，有像样的硬件，并且使用有可用工具链的零件。此外，Rigol 在那些有可能入侵他们的示波器的人当中很受欢迎。使用开源或免费工具，Xilinx FPGA 和 ARM 处理器非常容易使用。

我们已经看到了几个[开放范围设计](https://hackaday.com/2016/10/06/open-design-oscilloscope-could-be-almost-free/)，但是从零开始开发和对已经建成的东西进行逆向工程是不同的动物。我们也看到了【达夫·琼斯】[对 DS1054Z](https://hackaday.com/2014/10/22/how-to-reverse-engineer-featuring-the-rigol-ds1054z/) 进行逆向工程的细节。我们确信这将对 tmbinc 的努力有很大帮助。我们希望 Hackaday 的读者能够响应号召，帮助开发一些开源软件。看看社区是否能胜过制造商将会很有趣。