# 跑步者的 RFID 芯片的照片

> 原文：<https://hackaday.com/2016/06/30/die-photos-of-a-runners-rfid-chip/>

像公路赛这样的大众参与的体育赛事对其记录保持者来说是一个重大的问题。让一万名计时员在终点线的秒表旁徘徊是不可能的，那么他们是如何记录每个跑步者的时间的呢？答案就在每个跑步者佩戴的围兜里面的 RFID 芯片上，当跑步者冲过终点线时，芯片会被读取，以确保他们的时间在数百名其他参与者中被记录下来。

[Ken Shirriff]从旧金山的“Bay to Breakers”比赛中得到了一条围兜，然后[开始拆卸以暴露它的秘密](http://www.righto.com/2016/06/inside-tiny-rfid-chip-that-runs-san.html)。

[![The foil antenna pattern.](img/8253fa918ebdffb4d07dbeb8effe3dca.png)](https://hackaday.com/wp-content/uploads/2016/06/antenna.jpg)

The foil antenna pattern.

剥去 RFID 组件的泡沫覆盖物，露出了 860-960MHz 超高频带的箔天线，其中心是微型 RFID 芯片。天线很有趣，它是一个相当简单的宽带偶极子折叠起来，看起来像一个匹配的短截线排列和一个箭头装置，这可能是为了美观而不是实用目的。他将该芯片命名为 imp inj Monza 4 T1，其数据手册包含了我们期望提供更好性能的天线参考设计。

经过一些试火环氧树脂删除微小的芯片被发现和拍照。这是一个由三部分组成的设备，功率收集和模拟无线电部分，承载有效载荷的非易失性存储器，以及完成工作的有限状态逻辑机器。这不是一个合适的处理器，相反，它只包含返回有效载荷的任务所需的逻辑。

最后，他用一张 80 年代 8051 系列微控制器上的芯片的对比照片(大约有一粒盐大小)来展示其微小的尺寸和在这几十年间实现的密度进步。

由于 RFID 设备正在成为日常生活中无处不在的一部分，通过像这样的拆解来了解它们是很有趣的。这里的芯片与普通应用中的芯片有所不同，因为它使用更高的频率，我们很想知道在终点线激活它所需的射频场强。了解系统如何处理碰撞也很有趣，因为许多跑步者同时经过阅读器，无线电波上肯定有很多 RFID 聊天。

我们以前介绍过[Ken]的工作，包括他对 Clive Sinclair 1974 年的科学计算器的[逆向工程，以及他对 TL431 电压基准](http://hackaday.com/2013/08/30/ken-shirriff-completely-reverse-engineers-the-1974-sinclair-scientific-calculator/)内部工作原理的[解释。虽然我们在这些页面上已经](http://hackaday.com/2014/05/26/ken-shirriff-explains-the-tl431/)[了很多 RFID 项目](http://hackaday.com/tag/rfid/)，但这似乎是我们报道的第一个拆除项目。