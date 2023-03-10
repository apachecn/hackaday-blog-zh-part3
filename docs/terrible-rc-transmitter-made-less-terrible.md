# 可怕的遥控发射器变得不那么可怕了

> 原文：<https://hackaday.com/2018/03/27/terrible-rc-transmitter-made-less-terrible/>

不言而喻，我们并不反对偶尔一次精心的故障排除和修复，事实上这是我们在这里讨论的最常见的事情之一。事实证明，人们并不太喜欢被敲诈，有很多聪明人会努力工作，以免把最喜欢的东西扔进垃圾桶。我们不能因此责备他们。

[![](img/6725bef5697e8d1ae1e9264a05d710fc.png)](https://hackaday.com/wp-content/uploads/2018/03/craprc_detail.jpg) 但是我们不得不说，我们一般不会看到那种对某个*全新*的东西的精心修理。不幸的是，这正是[Marek Baczynski]在试图为他的 YouTube 频道“dronelab”审查新的 iRangeX 发射机时不得不做的事情。他发现了一个设计和构造如此糟糕的发射器，以至于他不得不[解决一系列问题](https://www.youtube.com/watch?v=KSeuZGpuaSQ)来使这个东西变得可以忍受。正如你所料，他并没有建议任何人跑去捡这个。

最大的问题是万向节是如何构造的根本缺陷。由于电位计和操纵杆本身之间的表面配合不良，控制器的精度非常低。当操纵杆松开时，电位计甚至不会归零。一些胶带用于紧固连接，使控制器可用，但当精确控制基本上是该设备的全部要点时，如此差的公差是难以原谅的。

其他问题需要更多的调试来解决。TX 打开时发出绝对可怕的尖锐声音，但[Marek]确信他在嘈杂的声音中听到了一点旋律。通过示波器输入信号，他能够证实自己的怀疑。事实证明，TX 中使用的蜂鸣器有一个内置的音调发生器，可以覆盖预期的旋律。切换到一个基本的蜂鸣器解决了这个问题。类似地，如果收音机最近被关闭，它也不会打开，这一问题被追踪到一个错误值的电阻器。将一个~~更高~~更低的电阻放在它的位置上也解决了这个问题。

很难想象这个设备是如何带着这么多错误或不合适的组件出厂的，但我们在这里。并不是说这在任何价位上都是可以接受的，但正如[Marek]在视频中指出的那样，这种收音机并不便宜。对于将近 90 美元，期待一些实际可行的东西似乎不是不合理的。

这不是他第一次让“便宜的”钢筋混凝土硬件经受考验。我们最近报道了他为量化不同传输器的延迟所做的努力。随着 [RC 发射器世界的竞争越来越激烈](http://hackaday.com/2017/11/20/can-commodity-rc-controllers-stay-relevant/)，像这样的详细分析有助于将[真正的齿轮与玩具](http://hackaday.com/2017/12/18/frankendrones-toy-quads-with-a-hobby-grade-boost/)分开。

 [https://www.youtube.com/embed/KSeuZGpuaSQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/KSeuZGpuaSQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

