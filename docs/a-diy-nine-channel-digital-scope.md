# DIY 九通道数字示波器

> 原文：<https://hackaday.com/2018/03/22/a-diy-nine-channel-digital-scope/>

当您只有一个 FPGA 评估板时，您是否发现自己需要一个九通道示波器？不要绝望，[米格尔天使]已经覆盖了你。在试图弄清楚 RAM 控制器内核的内部工作原理时，他意识到他需要并行捕获大量信号，于是他发明了这个 9 通道数字示波器。

该范围通过 JavaScript 应用程序和以太网进行远程控制。图形输出以全高清 VGA 信号的形式提供，因此很容易看出发生了什么。将采样数据下载到控制计算机进行分析的工作正在进行中。[Miguel]在 Arty A7 开发板上运行他的实现，该开发板目前售价约为 100 美元，但该设计可转移到其他平台。代码和一些文档可以在 GitHub 上找到，休息后还有一个演示视频。

 [https://www.youtube.com/embed/rSdEprgKkq4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rSdEprgKkq4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



示波器在黑客传说中占据着特殊的位置，无论是模拟自制的，用于播放[地震](https://hackaday.com/2014/12/29/ultimate-oscilloscope-hack-quake-in-realtime/)的单元，还是被骗在规范之外工作的[。最后一个甚至给出了建议使用与这里类似的 FPGA 的注释。](https://hackaday.com/2015/07/21/fast-adc-for-laser-lab/)