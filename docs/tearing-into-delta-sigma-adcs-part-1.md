# 闯入德尔塔适马 ADC

> 原文：<https://hackaday.com/2016/07/07/tearing-into-delta-sigma-adcs-part-1/>

毫不奇怪，模数转换器(ADC)现在采用多种技术来实现比更简单的转换器更高的速度和分辨率。进入δ-适马(δ∑)ADC，它结合了多种技术，包括过采样、噪声整形和数字滤波。这并不是说，你需要几个芯片来实现这一点，这些天的单芯片德尔塔-适马 ADC，非常小，只需几美元。有时它们被称为适马-德尔塔(≘δ)只是为了混淆视听，我赞同这一措施，因为在工程界已经没有足够多的混淆来源了。

 [https://www.youtube.com/embed/SFAS8nE4_ZM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/SFAS8nE4_ZM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我要把这个分成两部分。我将讨论一些理论，展示展示德尔塔-适马特性的构建，以及何时你可能想要使用它们。

## ADC 架构

从下图中，我们可以看到包括德尔塔-适马在内的四种最流行的 ADC 技术。我们在上一篇文章中讨论了合成孔径雷达、闪光灯和双斜率相机，每个相机都有自己擅长的领域。适马-德尔塔提供了高分辨率和中等吞吐量的组合。

[![Architecture](img/54c8b091c962147d6f911be1b15a22c6.png)](https://hackaday.com/wp-content/uploads/2016/06/architecture.png)

ADC Architecture Comparison

## 德尔塔-适马框图

δ-适马转换器的框图包括三个主要部分:δ-适马调制器，以及由积分器和抽取器组成的两部分数字滤波器。

[![Block Diagram](img/ed537a6eaa895ed9b930dc5b0f0c6750.png)](https://hackaday.com/wp-content/uploads/2016/06/block-diagram.png)

Delta-Sigma ADC Block Diagram

调制器的工作是将模拟输入转换成单比特调制的数字流。积分器将该单个比特流累积成多比特值，该多比特值表示信号的平均值，但是具有大量额外信息。最后，抽取器移除多余的不需要的信息，从而产生精确但符合正确的最小尺寸的输出。

## 德尔塔-适马调制器

δ-适马调制器是 ADC 的核心，负责对输入模拟信号进行数字化处理，同时通过过采样和噪声整形等多种技术降低噪声。

[![modulator](img/4c7f1f6b4d6d5f840edf04bcc141957f.png)](https://hackaday.com/wp-content/uploads/2016/06/modulator.png)

Delta-Sigma Modulator Block Diagram

如框图所示，δ-适马调制器由一个差分放大器、一个积分器、一个 1 位比较器和一个开关组成，前者对输出反馈求和，后者用作噪声整形，消除低频噪声，后者有效反馈上一次采样结果的反相形式。由于反馈路径，数字输出代表样本之间的信号差异。

 [![scope](img/8ed927f30e7abe0ca235672d4a3aa3bd.png "scope")](https://hackaday.com/2016/07/07/tearing-into-delta-sigma-adcs-part-1/scope-29/)  [![average](img/c43733f1feca998512f0b70bfdc4cd2e.png "average")](https://hackaday.com/2016/07/07/tearing-into-delta-sigma-adcs-part-1/average/) 

为了证明数字哈希中确实隐藏着正弦波，我设置示波器对几个样本的输入进行平均。

## 量化噪声

在任何 ADC 中，由于量化过程的不准确性，都存在噪声或误差项，称为……等等……量化噪声。这实质上是实际值与 ADC 采样的感知值之间的差异。

[![](img/b78bc400cf838bcb193dcadde3ba3f2d.png)](https://hackaday.com/wp-content/uploads/2016/07/quantizatio-error-sidebyside.png)

Source:Wikipedia

ADC 的分辨率越高，噪声就越小。这一点是正确的，我们可以从数学上说，ADC 的有效位数(ENOB)可以由信号幅度与量化噪声幅度之比(称为信噪比)来确定。注意，为了讨论的目的，我忽略了所有其它噪声和非线性来源。

```
ENOB = (SNR-1.76)/6.02db
```

同样，我们可以根据 ADC (N)的分辨率预测量化噪声引起的信噪比

```
SNR = (6.02 x N) + 1.76db
```

## 频域

为了显示信号相对于噪声的幅度，我们可以查看频域中的一切，例如频谱分析仪的输出。当在频域中观察时，显示器的左侧通常代表最低频率，而高频在右侧。信号的振幅由顶部振幅较大的高度表示。这不要与我们通常在示波器上看到的时域相混淆。

[![Main: Frequency Domain Insert: Time Domain](img/dcf6e171b0fa25e1fa5f0629f618035c.png)](https://hackaday.com/wp-content/uploads/2016/06/frequency-time.gif)

Main: Frequency Domain
Insert: Time Domain

这里，频域是大显示屏，时域在右下角的插图中。改变频率会导致“驼峰”在主显示屏上从左向右移动，而这种效果可以在时域中被视为周期时间的变化。

## 过采样

一种非常有效的降噪技术是提高采样频率，这种技术称为过采样。这具有将量化噪声分散到更大部分频谱上的效果。在接下来的步骤中，应用滤波器来去除仅由我们引入的噪声占据的频谱部分中的噪声。因此，虽然它并没有完全消除噪声，但它降低了信号附近目标区域的噪声幅度。一个基本的经验法则是，采样频率每增加 4 倍，有效位数(ENOB)将增加 1。

 [![oversample-cropped](img/7d190a857e474c2f51a92c2cf5616ad3.png "oversample-cropped")](https://hackaday.com/2016/07/07/tearing-into-delta-sigma-adcs-part-1/oversample-cropped/)  [![oversample2](img/c66f2b62e5190e5a3ce26121e29f88cd.png "oversample2")](https://hackaday.com/2016/07/07/tearing-into-delta-sigma-adcs-part-1/oversample2/) 

这里我们可以看到过采样的作用:注意采样时钟从 5Mhz 变为 20 Mhz 时噪声水平的变化。

## 噪声整形

![noise-shape-cropped](img/d6a3bcf49fc10f89fc5c8c47864bb71a.png)δ-适马 ADC 利用了这种降噪技术，但又进一步利用了一种称为噪声整形的技术。由于δ-适马调制器使用一两个积分级，因此它具有自然的流量整形效果，低端的噪声以牺牲频谱的高端为代价得到降低。同样，我们并没有完全消除噪声，但它降低了信号附近目标区域的噪声幅度。

使用 ADC 评估软件显示噪声整形。

[![noiseshape 3](img/026c4dacd9fb21a361812b1340a300b7.png)](https://hackaday.com/wp-content/uploads/2016/06/noiseshape-3.png)

这些技术的结合是 Delta-适马 ADC 高分辨率的基础(记住低噪声允许高分辨率)。

这些是德尔塔-适马 ADC 工作原理背后的基本概念。在本系列的下一部分，我将演示如何创建数字滤波器，并展示一些实际结果。这里有一个硬件镜头来吊起你的胃口。订阅我们的 YouTube 频道，关注下一期的头版。你也可以查看一下[比尔赫德原创视频播放列表](https://www.youtube.com/playlist?list=PL_tws4AXg7asaM6F72G_G_6g_e-BxXQn3)，直到下一个准备好。

如果你有任何问题，请在下面的评论中告诉我，我会在下一篇文章中给出答案。

![](img/394fc6505baced2af1654e20621679f5.png)