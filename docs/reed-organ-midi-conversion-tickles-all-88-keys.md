# 簧片风琴 MIDI 转换发痒所有 88 个键

> 原文：<https://hackaday.com/2017/09/13/reed-organ-midi-conversion-tickles-all-88-keys/>

你在高中做什么？很可能它远没有把簧片风琴变成 MIDI 设备那么酷。即使你成功地做到了，你是通过机械地控制所有 88 个键做到的吗？没想到会这样。

簧片风琴是一种键盘乐器，它将流动的空气通过一组调音的铜簧片来产生音符。大多数都是相当复杂的事情，有多个键盘和额外的控制，但[威廉·希勒]免费获得的那个看起来几乎和钢琴一样。即使有免费的仪器，[Willem]在这个项目上也投入了大约 500 美元。几乎一半的预算都花在了螺线管和驱动 MOSFETs 上——毕竟每个按键都有一个螺线管。每一个都需要小手术来减少咔嗒咔嗒的声音，这些声音对音乐体验没有任何帮助。[Willem]为 MOSFETs 设计了定制的驱动板，每个板有 16 个通道，并添加了几个电源来为所有那些饥饿的螺线管和三个 Arduinos 供电，以满足演出的需要。下面的视频显示了器官正在与活泼的“大黄蜂的飞行”进行压力测试；有点炫耀没什么不好。

[Willem]的构建为 MIDI 领域又增加了一种乐器。我们之前已经报道了很多，从[手风琴](https://hackaday.com/2017/02/01/converting-an-acoustic-accordion-to-midi-oh-the-complexity/)到[口琴](https://hackaday.com/2017/05/21/a-midi-harmonica/)，甚至[一个非常烦人的警笛](https://hackaday.com/2017/01/29/annoy-your-neighbors-with-midi-musical-siren/)。

 [https://www.youtube.com/embed/36Er-6ZRR6Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/36Er-6ZRR6Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

