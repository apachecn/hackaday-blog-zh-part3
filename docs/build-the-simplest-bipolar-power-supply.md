# 构建最简单的双极性电源

> 原文：<https://hackaday.com/2016/10/29/build-the-simplest-bipolar-power-supply/>

你需要多少个集成电路来构建一个将市电交流电转换成稳定的 DC 电压的电源？你会相信吗，一个也不会？我们刚刚看了【当前来源】(嵌入下面)的[这个视频](https://www.youtube.com/watch?v=0iDCsrMM7M0)，他正是在那里构建的。如果你想看二极管电桥以及半波和全波整流器的精彩回顾，你应该去看看。

首先，[TCS]介绍了整流的基本原理，并在示波器上很好地演示了增加输出电容如何平滑纹波。(提示:越多越好。)然后就关了建。最终结果是一个非常简单的非稳压电源——只是一个二极管桥，输出端有一些电容——但通过使用非常大的电容，他可以将纹波降低到几毫伏的范围内，成为一个恒定的负载。

该电路的输出电压*将*取决于平均电流，但对于基本静态负载，该电路应该足够好地工作，并且简单地扔出巨大的电容器来解决问题是有吸引力的。(我们会在某个地方放一个线性调节器。)

不过，对电路设计吹毛求疵并不是你看这个视频的原因。是因为你想学点东西。看看他其余的视频。[TCS]才刚刚起步，但看起来这将是一个值得关注的频道。

 [https://www.youtube.com/embed/0iDCsrMM7M0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/0iDCsrMM7M0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

