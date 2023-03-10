# 构建波表合成器

> 原文：<https://hackaday.com/2017/02/05/building-a-wavetable-synth/>

每个学期，在康奈尔大学[Bruce Land]的一个电子实验室里，学生们会组成团队，就他们希望为最终项目构建什么提出一些想法。学生们总是会挑选他们认为酷的东西。关于伊恩、乔瓦尔和巴拉兹，我们只知道他们中的一个是合成头。我们是怎么知道的？他们为他们在 ECE4760 的最终项目建造了[一个可编程序波表合成器](http://people.ece.cornell.edu/land/courses/ece4760/FinalProjects/f2016/ijh6_jjm448_bas332/ijh6_jjm448_bas332/ijh6_jjm448_bas332/index.html)。

首先，什么是波表合成器？它不是对正弦波、三角波和方波进行加法、减法和调制。我们认为，这是模拟高级实验室的领域。波表合成器不是怪异的反向 FFT 的深度应用——那是 FM 合成。波表合成只是以不同的速度播放单个波形——一个任意波形。它在 80 年代和 90 年代很流行，所以它是现代微控制器的一个很好的应用。

当然，构建的难点是从微控制器中获取波形，混合它们，并对它们进行调制。这是一门实验课，所以本学期早些时候学习的一些弹奏 DTMF 音调的技巧非常有用。项目中使用的微控制器是 PIC32，以 32 位定点方式执行所有运算。尽管最终的音频输出是 12 位分辨率，但在 16 位和 32 位之间进行计算的差异是显而易见的。

合成器是没有用的，除非它有某种用户界面，为此，人们求助于一个小的 TFT 显示屏、几个盆和几个按钮。这是一个完整的 GUI 来设置音序器播放的所有参数、波形、速度和音符。从该项目的视频来看(见下图)，对于一台产生哔哔声和 bloops 的机器来说，这东西听起来相当不错。

 [https://www.youtube.com/embed/-MwzoiNMvcI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-MwzoiNMvcI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

