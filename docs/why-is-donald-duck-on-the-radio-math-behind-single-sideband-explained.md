# 为什么唐老鸭会在收音机上？单边带背后的数学解释

> 原文：<https://hackaday.com/2018/01/01/why-is-donald-duck-on-the-radio-math-behind-single-sideband-explained/>

调幅是通过无线电波传送声音的最早方式。这很有意义，因为调制信号很容易，解调信号也很容易。碳麦克风足以对 AM 信号进行粗略调制，二极管——甚至是一块天然晶体——也足以对其进行解调。在广播电台之外，大多数 AM 用户迁移到单边带或单边带。在调幅接收器上听起来像唐老鸭，但稍加努力，它听起来几乎和调幅一样好，在许多情况下甚至更好。如果你想更好地了解单边带是如何传输音频的，看看关于这个主题的视频。

该视频涵盖了你可能已经知道的数学知识:AM 有一个载波和两个相同的边带。单边带抑制载波和一个冗余边带。但是它背后的数学是优雅的，尽管你可能应该知道一些三角学。不过不要担心。在视频的最后，有一个实用的演示，即使你在数学方面有困难，也会有所帮助。

如果你认真学习电气工程，把信号作为数学方程来处理是很重要的。例如，您可以用以下等式模拟一个纯正弦波:S(t) = A sin(2*pi*F*t)其中 A 是幅度，F 是频率(单位为赫兹)，t 是时间。[试试看](https://www.wolframalpha.com/input/?i=S(t)%3D20*sin(2*pi*1000*t))。在该示例中，频率为 1 kHz，幅度为 20，但是您可以调整这些值，看看会发生什么。如果你在正弦函数的自变量中加入一些东西，你将[改变波的相位](https://www.wolframalpha.com/input/?i=S(t)%3D20*sin(2*pi*1000*t),+S(t)%3D20*sin(2*pi*1000*t%2B0.5))。如果你照做了，你应该对视频没有问题。

这种数学不仅仅适用于解决家庭作业问题。这和你需要用计算机或数字信号处理器进行合成的数学运算是一样的。如果你想深入了解，我们前面谈到过[相角数学](https://hackaday.com/2017/06/15/imaginary-ac-circuits-arent-really-complex/)。

 [https://www.youtube.com/embed/l7n58h-Zj3I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/l7n58h-Zj3I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



但是等等，这个奇怪的标题是怎么回事？你曾经在调幅广播中听到过单边带信号吗？大多数人形容它听起来像唐老鸭。在这个 mp3 文件的[的大约 20 秒标记处听，在那之后，也是上边带(另一种 USB ),但是在频率之外，你会听到那个著名的声音。如果这一切都是陌生的，你需要](http://www.hamuniverse.com/ssbaudio.mp3)[探索 AM](https://hackaday.com/2016/06/07/am-the-original-speech-transmission-mode/) 的语音传输起源。