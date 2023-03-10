# 穷人的时域反射计

> 原文：<https://hackaday.com/2016/04/15/poor-mans-time-domain-reflectometer/>

时域反射仪(TDR)是测试长电缆的必备工具。这个想法很简单:沿着电缆发送一个脉冲，然后监听远端的反射。问题是那个讨厌的宇宙常数，光速。

光速成为问题的原因是，在传统系统中，脉冲需要在反射之前完成。此外，时间就是分辨率，因此 1 GHz 采样速率可提供约 10 厘米的分辨率。[Krampmeier]有不同的设计。他发送可变长度的脉冲，并测量输出脉冲和反射脉冲之间的重叠。与传统方法相比，该方法允许更简单的设计。

有一个奇特的部分:ECL 异或门。ECL 是一个逻辑家族，它在有源区使用晶体管来实现非常快的开关速率。通过在 XOR 门的一个输入端使用 RC 低通滤波器并用脉冲驱动它，该器件可以产生各种快速脉冲长度。

[Krampmeier]提交了一个竞赛的设计，但将在竞赛结束后提供更多细节(在同一讨论线程中还有更多细节)。此外，其他人提到了其他资源的链接，包括一个带有微芯片 PIC 的廉价 TDR([Krampmeier]项目使用了 ST ARM 板)和来自[w2ew]的必修视频[。](https://www.youtube.com/watch?v=Il_eju4D_TM)

当然，我们之前已经讨论过 TDR。我们甚至研究了[一个棘手的案例](http://hackaday.com/2015/07/27/find-and-repair-a-230kv-800amp-oil-filled-power-cable-feels-like-mission-impossible/)，在那里它实际上并没有多大帮助。

 [https://www.youtube.com/embed/mHjLV4RqYCw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mHjLV4RqYCw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

