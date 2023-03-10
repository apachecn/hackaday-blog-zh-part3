# 本周失败:设计宽带无线电的陷阱

> 原文：<https://hackaday.com/2016/08/05/fail-of-the-week-the-pitfalls-of-designing-a-wideband-radio/>

如果您对 RF 领域感兴趣，那么您就不需要讲述经济实惠的软件定义无线电技术的出现所带来的无限新可能性。如果你是一名设计师或建筑师，你可能会很容易相信这些无线电可以减少射频设计工程师面临的一些问题。毕竟，这种棘手的信号处理工作已经转移到代码中，因此 RF 工程师剩下的唯一工作应该是填补天线与 ADC 或 DAC 之间不那么大的差距。

在某些情况下，这是真的。如果您正在为相对较窄的频段设计 SDR 前端，例如业余频段等单一频率分配，所面临的挑战与传统无线电前端面临的挑战基本相同。因此，最简单的 SDR 完全在家庭构建者的能力范围之内，例如，将低于 100kHz 宽的无线电频谱段转换为质量不错的计算机声卡的低于 100kHz 基带音频带宽，该声卡同时充当 ADC 和 DAC。你只需要设计一套不太宽的滤波器，你要用的集成电路也不会特别奇特。

但是如果你设计的 SDR 不是一个简单的窄带设备会怎么样呢？[Chris Testa，KD2BMH] [在今年的代顿大会上发表了演讲](https://www.youtube.com/watch?v=ZK_qLSKlqIY&t=34m37s)回顾了他在过去几年的 50MHz 至 1GHz 带宽 [Whitebox 手持 SDR](http://radio.testa.co/index.html) 项目工作中所犯的一些错误和遇到的陷阱。它不是传统意义上的 FoTW，因为它不是一个不光彩的失败，而是对一个未来的射频工程师可能犯的许多错误的坦率而迷人的检查。

他讲话的视频可以在休息时间下面找到，由现在的火腿电台提供。[Chris]的演讲是[Bruce Perens，K6BP]之后的一个更长的演讲的一部分，你们有些人可能会从他的活动中认出他，但他没有谈到数字语音和 SDR。我们在大约第 34 分钟的时候开始追上[克里斯]，但是[布鲁斯]的演讲本身几乎可以写一篇文章..

 [https://www.youtube.com/embed/ZK_qLSKlqIY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=2077&wmode=transparent](https://www.youtube.com/embed/ZK_qLSKlqIY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=2077&wmode=transparent)



如果 SDR 对你来说是一门外语，也许你应该阅读[我们的 Hackaday Dictionary 文章解释技术](http://hackaday.com/2016/05/30/hackaday-dictionary-software-defined-radio-sdr/)，如果你对 RF 设计感兴趣，你也应该听听 [HackRF 创造者【Michael Ossmann】关于这个主题的演讲](http://hackaday.com/2016/03/23/michael-ossmann-makes-you-an-rf-design-hero/)。

谢谢[亚采克]的提示。