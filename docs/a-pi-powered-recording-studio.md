# Pi 驱动的录音棚

> 原文：<https://hackaday.com/2016/03/13/a-pi-powered-recording-studio/>

在 90 年代中期，你在 Tascam 盒式磁带上录制了你的乐队的小样。这些便宜得惊人的四声道便携式录音室的技术含量很低，足以给一支自称“有点像珍珠果酱，但有一架钢琴”的乐队带来真实性。十年后，这些录音机消失了，就像你成为摇滚明星的梦想一样，取而代之的是便携式数字录音棚。

Raspberry Pi 已经存在，Linux 音频栈的状态比十年前好得多，现在可以建立自己的独立录音室了。这正是[丹尼尔]在我们的树莓派零度竞赛中所做的，[并且可以预见他会把它叫做皮斯特迪奥](https://hackaday.io/project/9530-pistudio)。

虽然技术已经从盒式磁带发展到 CompactFlash 卡，再到硬盘驱动器，但这些四轨迷你录音室的设计自 20 世纪 80 年代推出以来一直没有真正改变。有四个通道，每个通道都有一个推子、平衡、均衡器和一个线路输入和 XLR 插孔。有主控制，几个 VU 米，如果技术是数字的，一对 MIDI 插孔。因为[Daniel]在这个项目中使用了 Raspberry Pi，所以他加入了一个 LCD 来提供一个很棒的用户界面。

和所有的数字录音机一样，钱在模数转换器里。【丹尼尔】使用的是 24 位、216kHz、四通道芯片，[德州仪器的 PCM4204](http://www.ti.com/product/PCM4204/description) 。这足以迷惑一个音响发烧友的耳朵，尽管这么多的数据需要一个硬盘。[好事必有萨塔](https://hackaday.io/project/9530-pistudio/log/31417-there-will-be-sata)。

虽然你可以花几百美元买一个八通道固态录音机，而且[丹尼尔]肯定会在这个项目上投入更多，但对于一个非常非常有用的设备来说，这是一个无处不在的 Linux 计算机的伟大应用。

* * *

![Raspberry_Pi_LogoSmall](img/87d7e34f7ac8cc3ae6c8619ad96c149e.png)

树莓派零竞赛由 Hackaday 和 Adafruit 主办。奖品包括 Adafruit 的树莓派零和 Hackaday 商店的礼品卡！
[查看所有参赛作品](https://hackaday.io/submissions/adafruitpizerocontest/list) || [现在就进入你的项目吧！](https://hackaday.io/contest/9326-adafruit-pi-zero-contest)