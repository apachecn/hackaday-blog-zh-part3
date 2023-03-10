# 一个有 38 年历史的声码器项目

> 原文：<https://hackaday.com/2018/07/06/a-38-year-old-vocoder-project/>

很难记得几十年前，电子杂志——互联网出现前的博客——有许多基于模拟处理的音频电路。例如，音乐合成器很受欢迎，因为微控制器很贵，无法像今天使用的那样执行数字信号处理任务。[Julian]一直试图从那个时代的 ETI 杂志中建立一个声码器。一路上，他在[制作视频](https://www.youtube.com/watch?v=8y0wqX4Nla0)，记录他的发现以及他是如何解决问题的。

该电路产生特定输入频率的电平。它通过一个双运放带通滤波器、一个双运放整流器和一个运放低通滤波器来实现。每个频段有五个运算放大器(共有 14 个频段)，外加支持电路。而这还只是输入部分！如今，您只需对信号进行采样，然后进行快速傅里叶变换(FFT)就能获得相同的数据。

我们可以同情[朱利安]，因为看起来他断断续续地为此工作了很长时间。[播放列表](https://www.youtube.com/watch?v=YWUH-w-m1h8&list=PLjzGSu1yGFjXKZ5igKxwlgfGdy25yZoPN)有一些可以追溯到 2015 年的预备视频。之所以花这么长时间，部分原因可能是他在制作不同的分段，并以各种方式进行测试。因此，虽然项目还没有完全完成，但观察对各个部分的描述、测试以及他遇到的问题是很有趣的。虽然我们更有可能在真实的硬件上模拟和使用示波器，但构建真实的电路并使用 VU 仪表板来可视化它们的输出还是很有魅力的。

从旧的计划中建造东西肯定会出现一些奇怪的事情，这个项目也不例外。[Julian]注意到，在 14 个频段中，除了三个频段之外，所有频段都使用非常标准的双极性运算放大器。但其中三个频段使用基于 FET 的运算放大器。如果你猜是为了频率响应，那你就猜错了。三个频段在较高范围内，但有两个较高频段使用双极性器件。[Julian]正在征求为什么会这样的意见。我们立即意识到，双极性运算放大器需要额外的电阻来抵消输入偏置误差。但我们不清楚为什么这三个乐队一开始就很“特别”。在 YouTube 的评论中有一些关于这个的理论。

我们不会错过的一件事是缺少一个微控制器来处理用户界面。看看前面板上所有的控制器！这不仅是大量的布线，面板工作是实质性的。今天，你会有一个液晶显示器，几个菜单按钮和一个旋转编码器。

如果你想重温你的滤波器设计，[埃利奥特·威廉姆斯]做了[一整个系列的滤波器](https://hackaday.com/2017/03/08/dont-fear-the-filter-lowpass-edition/)，还有[[比尔赫德](https://hackaday.com/2015/01/13/universal-active-filters-part-1/)。这两个都可以给你一些背景，以进一步欣赏这个项目。

 [https://www.youtube.com/embed/8y0wqX4Nla0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8y0wqX4Nla0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

