# Kay Igwe 通过 SSVEP 解释大脑游戏

> 原文：<https://hackaday.com/2015/12/03/kay-igwe-explains-brain-gaming-through-ssvep/>

* * *

在超级黑客大会上，我们有一些令人难以置信的演讲者。哥伦比亚大学电子工程研究生凯·伊格维做了最后一次演讲。[Kay]曾在英特尔从事纳米技术和半导体制造工作。这些天，她花时间玩游戏，但不是用手。

我们中的许多人喜欢游戏，可能花太多时间在电脑、游戏机或手机上玩游戏。但是手不能使用的人呢，比如 ALS 患者？将游戏带给残疾人促使[Kay]致力于控制它，一种控制游戏的大脑界面。脑机接口调用脑电图(EEG)机器的图像。通常这意味着大量的电极，头发上的凝胶，以及淹没在噪音中的数据。

[Kay Igwe]正在探索一种非常有趣的现象，这种现象使用闪光来引出非常特定且容易检测的脑电波。这种类型的界面非常有前途，也是她在今年的 Hackaday 超级大会上演讲的主题。请查看她的演示视频，然后在休息后加入我们，深入了解她的工作细节。

 [https://www.youtube.com/embed/jt3awPRdgVc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jt3awPRdgVc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



![kayslide1](img/7235de5133078f8c8654dbf91e0827b1.png)[Kay]采用了一种与基于脑电图的系统略有不同的方法。她正在使用[稳态视觉诱发电位(SSVEP)](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC1880883/) 。SSVEP 是一个简单概念的长名称。视觉数据在位于大脑后部的枕叶进行处理。事实证明，如果一个人看着 50 赫兹的闪光，他们的枕叶会有 50 赫兹或其倍数的强电信号。高达 75 Hz 的信号，比有意识地识别为闪光的速度更快，仍然会在大脑中产生电“闪光”。该信号是由神经元对视觉刺激的反应而产生的。SSVEP 的伟大之处在于其信号比标准的 EEG 信号更容易检测。干接触在这里工作很好——不需要凝胶！

![kay2](img/4f3e5f1e699e023a46bca545da1ee359.png)【凯氏】电路是用于放大人体产生的低功率信号的经典设置。她使用仪表放大器 AD620 将信号提升至合理水平。之后，几个主动过滤阶段清理东西。最后，脑电波信号被发送到 Arduino 的 ADC 中。

Arduino 将数据数字化并传送到电脑上。【凯】用[处理](https://processing.org/)分析信号，显示输出。在这种情况下，她正在执行快速傅立叶变换(FFT)，然后分析大脑信号的频率。最后，输出以游戏的形式显示出来。

凯设计的视频游戏允许用户在屏幕上移动角色。这是通过观察两个闪烁的灯中的一个来完成的。一盏灯让玩家跑向右边，而另一盏灯让玩家向上移动。

[Kay]有很多控制它计划，从控制轮椅到无人驾驶飞机。我们希望她在哥伦比亚大学的研究生课程之间有时间完成所有的工作！