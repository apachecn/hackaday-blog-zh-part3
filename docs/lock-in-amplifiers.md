# 锁定放大器

> 原文：<https://hackaday.com/2017/09/27/lock-in-amplifiers/>

如果你有大约一个小时的时间，你可能想看看关于斯坦福研究所 SR530 锁定放大器的[Shahriar]视频(见下文)。如果你知道什么是锁定放大器，这仍然是一个非常有趣的视频，如果你不知道，那么它真的是一个必须看到的。

大多数时候，你会认为放大器只是一个以某种方式将小信号变大的电路——也就是说，增加电压或增加电流。但是，有一整类放大器是为抑制噪声而设计的，锁定放大器就是其中之一。[Shahriar 的]视频讨论了放大器背后的数学理论，展示了胆量，并演示了一些实验(包括测量声速)。

放大器背后的数学大部分是三角函数，尽管有一点微积分。想法是将参考频率与目标信号混合在一起。这将导致两个信号的和与差。随着时间的推移，积分信号将归零。

这可能不太直观，但考虑一下这个:由于[傅立叶分析](https://hackaday.com/2015/09/17/visualizing-the-fourier-transform/)，我们知道任何信号都可以分解成一束正弦波。因为正弦波有相等的正负偏移，如果你在整个周期内积分，它下面的面积为零。如果你的微积分生疏了，积分或多或少就是将曲线上无限薄的切片相加，得到曲线下的面积。由于正弦波的正负面积相等，因此下方的面积为零。

将输入归零的放大器不是很有用。然而，有一个问题。如果参考信号和输入信号相位不同但频率相等，那么差项将是一个不随时间变化的常数。当你对整个信号进行积分时，这个常数会显得很突出。

这是基本的想法。如果你想了解更多的细节，这个视频很好地解释了它，并在实践中展示了它。

如果您注意到 SR530 的框图，其中有许多 PLL，这是我们在之前讨论过的[主题。你可能想知道为什么不能用](https://hackaday.com/2016/03/23/unlock-the-phase-locked-loop/)[来过滤感兴趣的频率](https://hackaday.com/2017/03/08/dont-fear-the-filter-lowpass-edition/)。理论上，你可以。但正如[Shahriar]解释的那样，要从一个滤波器中获得同样的性能，需要一个不切实际的窄滤波器。

 [https://www.youtube.com/embed/rzzliN_vTKs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rzzliN_vTKs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

