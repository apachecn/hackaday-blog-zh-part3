# 回顾:锤装无焊覆盆子 Pi 引脚接头

> 原文：<https://hackaday.com/2017/01/16/review-hammer-installed-solderless-raspberry-pi-pin-headers/>

几天前，我们报道了为 Raspberry Pi Zero 用户设计的新产品[，这是一套无焊插头，采用了一种新颖的安装方法，包括锤子](http://hackaday.com/2017/01/09/give-your-raspberry-pi-a-good-hammering/)。我们怀疑它们是否能提供良好的接触，更愿意坚持使用可靠的焊接引脚。似乎很多人都同意，帖子的评论区变得有点热闹。该产品的创始人皮莫罗尼受到了大量的抨击，对此，他们表现出了应有的幽默。

很明显，这是一个有争议的产品，也许 Hackaday 的裁决是基于锤子方面的故事的一个小总结。因此，为了进一步了解所有这些大惊小怪的事情，我订购了一个 Pi Zero 和无焊引脚套件来亲自尝试。

[![The parts for the jig and connectors from Pimoroni.](img/20c99a4d15389364339fb8fd99c01cca.png)](https://hackaday.com/wp-content/uploads/2017/01/constituent-parts.jpg)

The parts for the jig and connectors from Pimoroni.

计划是在一个 Pi Zero 上安装引脚，然后通过反复插拔帽子来模拟一个热情的年轻人手中的典型电路板的寿命。为此，GertVGA 板代替了帽子，因为它是我手头上唯一一个带全尺寸连接器的 Pi 外设。

打开皮莫罗尼的袋子，我发现了一套他们的商标激光切割塑料件，两个尼龙螺栓，以及一套推入式插销和一个推入式插座。零件没有附带任何说明，相反，他们会将您发送到[他们的网站产品页面](https://shop.pimoroni.com/products/gpio-hammer-header)，在该页面上，他们有视频显示如何组装零件和安装连接器。

[![The bare pins, showing the eye-of-needle ends to the pins.](img/83e2d542401159fa6787410ad6f8665b.png)](https://hackaday.com/wp-content/uploads/2017/01/bare-pins.jpg)

The bare pins, showing the eye-of-needle ends to the pins.

引脚本身与长端的焊接引脚完全相同，但适合电路板的短端与更传统的引脚截然不同。每根针都被弄平并刺穿，形成类似手缝针眼的形状。

当提供给它们时，整个连接器不会穿过板中的孔，相反，它位于板的突出部分，并且不能容易地穿过它们。我马上就能看到夹具和锤子面临的任务，迫使这些钉子进入洞，这些洞不够大，不足以容纳它们。

[![The jig assembled, with the Zero and pins in place.](img/b20f697d36e47c3ff8d3ffd6b78f5cd1.png)](https://hackaday.com/wp-content/uploads/2017/01/assembled-jig.jpg)

The jig assembled, with the Zero and pins in place.

塑料部件形成一个夹具，将零点保持在适当的位置，并提供一片塑料作为引脚顶部的漂移，以及零点以下的几层以承受负载。同时，两个螺栓将不同部件上的孔与零上的孔对齐，并通过销装配过程将所有东西保持在适当的位置。

所有这些使我们干净利落地开始了锤打。他们的视频显示了沿着夹具的长度用针锤连续轻敲，所以我们的零点被放置到位，锤击开始。沿着连接器长度的每组抽头都使它前进了很小的量，所以我不得不尝试几次，检查每组之间的进度。在某一点上，连接器的两端比中间更深入电路板，因此有必要在中间多敲一点。另一个问题出现了:电路板有轻微的弯曲。如果我要做第二个，我会尽可能小心地把它减到最小。然而，一旦连接器沿其整个长度正确就位，弯曲就消失了。所需的锤击动作实际上非常轻，与其说是击打，不如说是轻敲。很可能，如果用同样的技术在一块木头上钉一个图钉，可能根本就不会把它敲得很深。

你可以在下面的视频中看到整个过程。用这种方式安装连接器肯定很快，我怀疑我能否用焊料匹配它。

 [https://www.youtube.com/embed/29Hd1F_89C4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/29Hd1F_89C4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[![Our Pi Zero test setup on a table at Oxford Hackspace.](img/f78c109b07d7a2c66c8728cb2baa1c69.png)](https://hackaday.com/wp-content/uploads/2017/01/pin-test-setup.jpg)

Our Pi Zero test setup on a table at Oxford Hackspace.

当零点从夹具上移除时，可以看到销很好地位于孔中，并且不能移动。运行一个小 Python 脚本，通过将 GPIO 引脚设为高电平和低电平来产生方波，发现它在所有可用引脚上都有效。

一切都很好，我已经安装了引脚，他们的工作。然而，一组引脚的意义在于，它们应该在器件的整个生命周期内可靠地工作。我不能为了一年的艰苦服务而把它交给一个渴望的孩子，因为我没有多余的一年来进行测试，但我可以通过反复连接和断开外围设备来模拟大量使用。一个 GertVGA 板代替了一顶帽子，因为这是我唯一一个带全尺寸 Raspberry Pi 连接器的板。参加牛津 Hackspace 社交之夜的游客看到了一个黑客抄写员反复从零开始插拔 GertVGA 超过 100 次，直到她的手指受伤。下面的加速视频只展示了这个过程的一小部分。

 [https://www.youtube.com/embed/vXIVljCDqj0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/vXIVljCDqj0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



在所有重复的 GertVGA 插入之后，引脚仍然严格地连接到零，当我在 GPIOs 上尝试时，我的 python 脚本奖励了我一个方波。所以我安装了插针，它们在中度滥用的情况下存活了一个晚上，连接完好无损。

总之，公平地说，我们在这里有点吃字，因为引脚已被证明是直接安装和重复使用足够可靠。焊接可能仍然是个人选择的方法，它们的安装需要非常小心，但这些推入配合引脚代表了一个可行的替代方案。带有夹具的完整套件重 6 英镑(约 7.50 美元)，比 Pi Zero 贵 1 英镑(约 1.25 美元)，但值得记住的是，它包括一个插座和引脚，虽然焊接连接器会更便宜，但如果你还没有它们，焊料和铁的成本会高得多。同样值得一提的是，Pi Zero 便宜得离谱，几乎所有配件看起来都很贵。

有趣的是，引脚和 PCB 孔边缘之间的张力是否会使孔随着时间的推移而拉伸或松弛，以及如果连接器使用多年，这是否会导致问题。修复是焊接连接器的简单情况，但这可能是一个问题。然而，这并不影响大多数购买这种产品的人所期待的即时效果。

如果你在你的 Pi Zero 上尝试过这个连接器，请在评论中告诉我们你的进展。不过请记住，在上面链接的前一篇文章的评论中，不知情的批评已经够多了，所以如果你想加入，请确保你有新的东西加入讨论。