# 猫咪喂食器有蒸汽朋克风格和 GMail 账户

> 原文：<https://hackaday.com/2017/11/10/cat-feeder-has-steampunk-flair-and-a-gmail-account/>

虽然人们常说“需要是发明之母”，但我们不能说这一直是我们在 Hackaday 的经历。你不需要搜索太久，就能在这个网站上找到一个绝对不在严格的必要性范围内的项目或黑客。但这是乐趣的一部分，这是这个网站不叫 AppropriateUseOfTime.com 的原因

但是当(山姆·斯托里诺)似乎无法阻止他的猫在凌晨 3 点嚎叫着吃晚饭时，他有了实现这一古老智慧的绝佳机会。他不仅设法把去当地家装店的管道岛之旅变成了一个看起来非常蒸汽朋克的自动喂猫器，而且他还抽出时间写了一系列特别详细的博客帖子，讲述他在这个过程中所学到的东西。

[![](img/e78b588d5f721bf0e12db973d91e5b5c.png)](https://hackaday.com/wp-content/uploads/2017/11/pifeeder_detail.jpg) 机器的心脏是大家最喜欢的 Linux 板，树莓派。你可能认为圆周率对于一个简单的计时器来说太过了，你是对的。与其只是按照设定的时间表把食物倒掉，【山姆】决定来点新奇的，想出一些 [Python 脚本来监控 GMail 收件箱](http://storiknow.com/automatic-cat-feeder-using-raspberry-pi-part-three/)，并在收到标题为“喂猫”的电子邮件时激活 feeder 硬件。然后，他使用 IFTTT 按照特定的时间表将适当命名的电子邮件发送到他的猫喂食器的 GMail 帐户。嘿，没人说过需要是简单明了的发明之母。

[在本系列的最后一篇文章](http://storiknow.com/automatic-cat-feeder-using-raspberry-pi-part-four/)中，【Sam】讲述了设备的硬件方面。铜管组成的框架，其中持有一个商业现成的干粮分配器。进料器是为手动操作而设计的，但通过连接一个连续旋转伺服系统[Sam]可以使它旋转起来，并通过 Pi 的 GPIO 引脚倾倒预先测量好的食物量。添加一些 PVC 管和配件可以将食物(至少在理论上)平均分配到下面的两个猫碗中。

如果你认为[山姆]可能在喂宠物这样简单的事情上花了过多的心思，请记住[他是一个非常好的伙伴](https://hackaday.com/2016/06/02/feeding-the-cat-reinventing-the-wheel/)。翻阅档案，[似乎猫科动物和黑客的交集](https://hackaday.com/2015/11/05/automatic-cat-feeder-dispenses-noms-wants-cheezburger/)散落着[极其复杂的装置](https://hackaday.com/2012/05/06/automatic-cat-feeder-made-with-recycled-laminator-parts/)。