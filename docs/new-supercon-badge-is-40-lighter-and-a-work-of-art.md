# 新的 SuperCon 徽章重量减轻了 40%,是一件艺术品

> 原文：<https://hackaday.com/2016/09/28/new-supercon-badge-is-40-lighter-and-a-work-of-art/>

[2016 Hackaday 超级大会](https://hackaday.io/superconference/)即将召开，今天我们好好看看硬件徽章。它是由[Voja Antonic]设计的——一位将出席会议的硬件创造传奇人物。我喜欢把他看作是东方集团的沃兹，他设计了[Galaksija 计算机](https://en.wikipedia.org/wiki/Galaksija_(computer))。这个徽章是嵌入式设计的一个美丽的例子。休息之后我们将深入探讨所有的细节。

[现在就买票](http://www.eventbrite.com/e/hackaday-superconference-2016-tickets-27343845177?aff=927badge)参加 48 小时的讲座、研讨会、Hackaday 颁奖晚会、徽章黑客活动等等。

 [https://www.youtube.com/embed/Gkd5RuY84p8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Gkd5RuY84p8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



该徽章包含一个 8×16 表面贴装 LED 矩阵、四个用户按钮(加上复位和从睡眠中唤醒)、红外通信和一个三轴加速度计，所有这些都由 PIC18LF25K50 驱动，由两节 AAA 电池供电，并通过 USB 编程。这是一个令人愉快的硬件满嘴。

![all-badges](img/d14afc1736131dbf3b25f684f85c4b18.png)

[Voja Antonic]的设计基于他为 4 月份的贝尔格莱德黑客日会议设计的徽章(如左图所示)。这是一个出色的徽章设计，[Voja]在这个设计上做了改进。我真的很喜欢边缘安装的单 AAA 电池支架，随着 LED 模块的更换，徽章的厚度减少了。他们还减少了重量，从 88 克减少到 52 克。耳朵敏锐的人会注意到，我在视频中错误地引用了 62 克，但较低的数字是正确的。

 [![2016-supercon-badge-front](img/7df1b380a9b753a886c494bbf45e090a.png "2016-supercon-badge-front")](https://hackaday.com/2016/09/28/new-supercon-badge-is-40-lighter-and-a-work-of-art/2016-supercon-badge-front/)  [![2016-supercon-badge-back](img/2adbf3ebd4cf900fd97102621882b3bb.png "2016-supercon-badge-back")](https://hackaday.com/2016/09/28/new-supercon-badge-is-40-lighter-and-a-work-of-art/2016-supercon-badge-back/) 

你在这里看到的会有一些变化。如果你仔细看，你可以看到 led 周围的丙烯酸挡板。在最后的徽章上，将会有一个丙烯酸扩散器。这个原型最初是在 6 月份生产的，上面印着错误的位置。SuperCon 将于 2016 年 11 月 5 日和 6 日在加利福尼亚州帕萨迪纳举行。

徽章是互动的。大会上的一个信息亭可以让你在徽章上存储你自己的滚动信息。如果你真的很聪明，你可以想出如何让你的徽章恶作剧其他人穿着。红外通信功能也是您参与加密挑战的方式。[Voja]在会议周围放置了一些徽章，上面存储了一些谜题，制造了一些乐趣。写一个程序到你的徽章上，与他们互动，并破译发回的信息。这在贝尔格莱德非常受欢迎，在 SuperCon 会更好！

背面的九针扩展头是该徽章设计用于黑客攻击的另一种方式。去年，我们与裸 PCB 硬件黑客[度过了一段美好的时光](http://hackaday.com/2015/11/20/the-best-conference-badge-hacking-youve-ever-seen/),提供对该徽章上硬件的直接访问非常重要。正如令人惊讶的[徽章黑客入侵贝尔格莱德会议](http://hackaday.com/2016/04/15/128-leds-5-buttons-ir-comm-and-a-few-hours-what-could-you-create/)，这个徽章正在运行引导加载程序。它管理所有硬件，提供对显示器、按钮和外围设备的内存映射访问。这意味着，如果你从来没有眨过 LED 灯，你会很快启动并运行。更有经验的程序员将不必陷入低级编码的泥沼，干瘪的专家可以吹灭引导加载程序并进入裸机(别忘了你的 PICkit)。

 [![2016-supercon-badge-circuit](img/75516e07f7c9c675b7a7073ea04d7a67.png "2016-supercon-badge-circuit")](https://hackaday.com/2016/09/28/new-supercon-badge-is-40-lighter-and-a-work-of-art/2016-supercon-badge-circuit/)  [![2016-supercon-badge-led-matrix](img/d943c131e9363f82dd33c93b9c555a45.png "2016-supercon-badge-led-matrix")](https://hackaday.com/2016/09/28/new-supercon-badge-is-40-lighter-and-a-work-of-art/2016-supercon-badge-led-matrix/) 

我想花点时间展示一下这个徽章的工艺。看看它的布局和美感——这是一件美妙的事情。现在仔细看看 LED 矩阵。当[Voja]第一次给我发送原型时，我以为有一些焊球粘在助焊剂上。不对。看起来像流浪猫毛或焊料飞溅的是一根细小的电线——忍者级的返工，在运到我这里之前由[Voja]手工完成。查看[他发布的其他项目](https://hackaday.io/voja)。

我喜欢这个徽章。它确实吸取了我们在过去两次会议上所做的最好的东西。想要得到它的唯一可靠的方法就是出现在 SuperCon。[现在就买票](http://www.eventbrite.com/e/hackaday-superconference-2016-tickets-27343845177?aff=927badge)！

### 散布消息

请帮助我们宣传 2016 Hackaday 超级大会。告诉所有你认识的人，并在你的社交媒体上分享 http://hackaday.io/superconference。谢谢！