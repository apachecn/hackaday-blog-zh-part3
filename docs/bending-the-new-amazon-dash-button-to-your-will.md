# 按照你的意愿弯曲新的亚马逊破折号按钮

> 原文：<https://hackaday.com/2016/07/26/bending-the-new-amazon-dash-button-to-your-will/>

大多数 Hackaday 读者都熟悉亚马逊破折号按钮，即使它尚未在他们的国家或地区出现。一个印有产品标志的 WiFi 按钮，当你按下它时，就会触发该产品的亚马逊订单。把它贴在你的洗衣机上，当你用完洗衣皂时按下按钮，一些洗衣皂就像变魔术一样出现了。你仍然不得不离开你的扶手椅去收快递员送来的肥皂，但是也许他们也在解决这个问题。

当然，隐藏在 Dash 按钮中的嵌入式计算机已经成为我们社区中非常感兴趣的主题，并且已经有相当多的重新利用和逆向工程示例的创造性使用。

今年早些时候，一种新的 Dash button 模型出现了。外观上很相似，但内部进行了全面的硬件更新。STM32 处理器将被 Atmel 部分取代，不幸的是，由于他们也对其通信协议进行了更改，该设备的大部分黑客也消失了。

[Evan Allen]写信给我们，介绍他按照自己的意愿弯曲新仪表板按钮的工作。他详细介绍了检索他们的 MAC 地址的主题，以及对现有攻击的修改，以允许按钮被拦截/重定向来触发他的 MQTT 服务器。这绝不是故事的结束，我们相信在适当的时候我们会看到新的 Dash 按钮的更多使用，但这只是一个开始。

如果你对新按钮的硬件感兴趣，那么[【马修·彼得罗夫】的拆卸绝对值得一看](https://mpetroff.net/2016/07/new-amazon-dash-button-teardown-jk29lp/)。除了 Atmel 芯片(发现是带有 ATWINC1500B 无线芯片的 ATSAMG55J19A-MU)之外，这些按钮现在还支持 AA 电池供电，并显著降低了功耗。我们真的，真的，需要 pwn 这个美味的新硬件！

我们之前已经讨论了相当多的 Dash button hacks，从[简单地捕获按钮按压](http://hackaday.com/2015/08/10/hacking-the-amazon-dash-button-to-record-whatever-you-want/)到完全打开它和[运行你自己的代码](http://hackaday.com/2015/08/12/amazon-dash-hack-it-to-run-your-own-code/)。让我们希望这个新版本将被证明是多才多艺的。