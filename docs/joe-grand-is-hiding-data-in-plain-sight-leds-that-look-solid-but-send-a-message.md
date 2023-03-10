# 乔·格兰德将数据隐藏在众目睽睽之下:发光二极管看起来很坚固，但却能传递信息

> 原文：<https://hackaday.com/2018/06/10/joe-grand-is-hiding-data-in-plain-sight-leds-that-look-solid-but-send-a-message/>

周四晚上真是一场盛宴。我在 HDDG 的聚会上见到了 Joe Grand 和 Kitty Yeung，他们都谈到了他们最近的工作。

Joe 向我们介绍了 optic spy T1，这是他最新的硬件产品，它起源于数据泄露的早期。还记得老式调制解调器上的灯在数据传输或接收时会闪烁吗？设计该电路最简单的方法是将状态 led 直接连接到串行端口的 RX 和 TX 线，但结果是将您的数据传播给任何有相机的人。你当然不能用你的眼睛看到闪烁如此快的光，但是用正确的齿轮你肯定能读出 1 和 0。乔用[的 BPW21R 光电二极管](https://www.vishay.com/photo-detectors/list/product-81519/)建造了一座向那个时代致敬的建筑。

通过光传输数据也是电视制造商几十年来一直在做的事情。他们是如何在充满光源的房间里工作的？它们过滤载波信号(通常为 38 kHz)。但是如果你对寻找任意信号感兴趣呢？乔的锦囊妙计是在没有载体的情况下，在很大的范围内实现的。这感觉有点像魔术，但即使你知道它是如何工作的，他对硬件的解释也值得一看！

 [https://www.youtube.com/embed/eqVKx9Yzk_Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=43&wmode=transparent](https://www.youtube.com/embed/eqVKx9Yzk_Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=43&wmode=transparent)



OpticSpy 从看似稳定的红色 LED 中提取数据的演示非常精彩。我很高兴乔也花时间走过这条赛道:

[![](img/25d053349b9c024aee531f0467abde69.png)](https://hackaday.com/wp-content/uploads/2018/06/joe-grand-optic-spy-amp-chain.png) 他提到，他并不总是能够扩展他的模拟设计能力，这是一个很好的项目。同样，我喜欢按照自己的方式完成原理图，它使用一个双级放大器来调理来自光学传感器的信号。最后一级是一个比较器，它输出数字信号。上面的截图中没有显示的是 FTDI 芯片，它接收这个信号并将其发送到你的串行终端。

[![](img/e7a0495e98c993d61e16b66008950cbb.png)](https://hackaday.com/wp-content/uploads/2018/06/composite-opticspy-joe-grand.jpg) 乔承认，如今很难找到泄露数据的 led，所以他不得不制造自己的人工来源。他的演示包括使用[视差开放会议徽章](https://hackaday.com/2015/09/14/the-open-hackable-electronic-conference-badge/)，一个由 Arduino 驱动的激光二极管，以及[一个隐藏在 USB 端口中的微控制器分线板](https://hackaday.com/2018/01/20/tomu-a-microcontroller-for-your-usb-port/)。四个 trimpots 允许调整舞台，这是乔为演讲必须做的事情，因为房间的前面被下午的太阳晒坏了。

在乔的介绍之后，杨小奇上台。作为一名应用物理学博士，Kitty 的才华跨越了许多领域，她可能会向你介绍自己是一名创造性的技术专家。你可能会在今年的湾区创客博览会上遇到她，她穿着肩扛式太阳能电池板，但她的可穿戴创作在创客社区之外非常有名，在 [2016 年旧金山时装周](https://artbyphysicistkittyyeung.com/2016/10/08/san-francisco-fashion-week-2016/)期间展示了多种设计。

![](img/c597951e607143aa03299439e6f47407.png)

在她的演讲中，凯蒂展示了一件令人惊叹的衣服，衣服上使用了发光二极管来照亮不同的星座。这些由手势控制，可以根据佩戴者的喜好重新训练。这种效果是令人愉快的，特别是因为它是为了配合她自己的绘画编织成的服装材料。

不幸的是，创造这样一件作品的劳动意味着这个想法很难规模化。在上图中，Kitty 正在展示她已经推向市场的三个设计。它们包括她的绘画，但不包括她喜欢添加到作品中的技术。我觉得她的公开挑战很有趣。现在，任何人都可以定制印花面料。你甚至可以订购混搭成分的服装，比如袖子的不同剪裁。Kitty 想知道如何将电子纺织技术引入低产量制造业，并期待工程界将其变为现实。

 [https://www.youtube.com/embed/Mi4uTDWIQ9E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=15&wmode=transparent](https://www.youtube.com/embed/Mi4uTDWIQ9E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=15&wmode=transparent)



不幸的是，我不住在旧金山，所以参加[硬件开发者的说教银河](https://www.meetup.com/Hardware-Developers-Didactic-Galactic/)是一种难得的享受，这是一个专注于开发电子硬件的月度聚会，每月在 Supplyframe 的旧金山办公室举行。总有像 Kitty 和 Joe 这样的特色演讲者，但出现的观众是一群在工业各个不同领域工作的工程师。如果你在这个地区，这是一个不能错过的活动。