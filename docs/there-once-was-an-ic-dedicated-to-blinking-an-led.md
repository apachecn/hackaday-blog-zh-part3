# 曾经有一个专用于闪烁 LED 的集成电路

> 原文：<https://hackaday.com/2018/01/04/there-once-was-an-ic-dedicated-to-blinking-an-led/>

今天你可以买到闪烁的发光二极管；一种简单的双引线元件，只需要一个电源就能产生均匀的闪光。它们看起来像任何其他 LED 一样，尽管塑料圆顶中嵌入了一个集成电路来完成所有闪光工作。

然而，曾经有一段时间，闪烁的 LED 是一件大事，以至于国家半导体公司为此生产了一种专用芯片。LM3909 拥有使用单节 C 电池使 LED 闪烁一年以上的能力。这部分现在已经停产很久了，所以[Dillon]已经使用小型 PCB 上的分立元件[实现了 LM3909 电路，该 PCB 设计用于接收引脚并适应原始电路的尺寸。](https://hackaday.io/project/29179-disintegrated-lm3909-15v-led-flasher)

你会问，他到底为什么会对重生的 LM3909 感兴趣？他不能用硬币电池做出 555 的闪光 LED，一个朋友提到了这个芯片，激起了他的兴趣。内部原理图在数据手册中([在他的项目的文件部分](https://hackaday.io/project/29179-disintegrated-lm3909-15v-led-flasher)中找到)，因此他能够使用通用器件相对容易地实现它。它仍然需要一个像原来一样的外部电容，但如果你想把它放在那里，板上有空间。

他制作了一个视频，我们把它放在休息时间下面，展示了这个设备的运行，证明它是一个原始设备的替代产品。使用分立器件再造经典芯片并不是什么新鲜事，我们最近为您带来了 2014 年生产的重生 PSU 调节器芯片。当你在玩硬币电池的时候，我们可以让你关注一下[硬币电池挑战赛](https://hackaday.io/contest/28283-coin-cell-challenge)。

 [https://www.youtube.com/embed/TYnx2c-3YMM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/TYnx2c-3YMM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢[德鲁·富斯蒂尼]的提示。