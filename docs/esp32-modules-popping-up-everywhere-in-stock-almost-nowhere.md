# ESP32 模块随处可见，几乎无处有货

> 原文：<https://hackaday.com/2016/11/02/esp32-modules-popping-up-everywhere-in-stock-almost-nowhere/>

我们知道等待新发布的电子零件是什么感觉。每天在你最喜欢的在线零售商那里点击刷新，阅读获得预览版的媒体发表的评论，甚至敢于从国外订购难以置信的廉价设备。ESP32 让我们中的许多人都在玩等待游戏，我们将与你坦诚相见——他们在大多数地方都缺货。但是，如果你足够努力地寻找，你可以找到一个。至少，您可以在我们撰写这篇 ESP32 硬件的快速综述之前找到它们。如果你喜欢听那些遥不可及的部分，那么继续读下去，你这个受虐狂！

## Espressif

制造 ESP-32 芯片及其支持固件的公司 Espressif 也在制造模块和开发板来支持它们。他们的模块是 ESP-WROOM32，不仅仅是第一个模块，它还充当芯片的[硬件设计参考](http://www.espressif.com/sites/default/files/documentation/esp-wroom-32_en.zip) (zip 文件)。他们还提供了模块的[数据表](http://www.espressif.com/sites/default/files/documentation/esp_wroom_32_datasheet_en.pdf) (PDF)。这一切都在那里，所以你可以运行他们的 Gerbers 和来源的部分，如果你想自己。

或者，你可以直接从 Espressif 订购[，这是我们从未尝试过的，或者你可以尝试在网上很多地方购买。Seeed](http://espressif.com/company/contact/pre-sale-questions) 是第一批进货的厂商之一，但现在已经缺货。Elecrow 声称他们有现货。

Espressif 还做了一个简单的开发板，这是我们收到的测试用的。这些在 [Adafruit](https://www.adafruit.com/products/3269) (每位顾客限购 1 件)有货，在 [Olimex](https://www.olimex.com/Products/IoT/ESP32-CoreBoard/) 也无货，但我们希望这种情况会很快改变。由于 Espressif 自己的模块供不应求，他们发布了一个参考设计，克隆制作人也站了出来，这是一件非常好的事情。让我们看看世界其他地方提供了什么。

## 一体式主板

无论您认为这些是开发套件还是 ESP32 突破，准备开始编程的完整最小设计应该包括电源调节器、USB/串行转换器、闪存、ESP32 芯片和天线。

[![nano32_3](img/4bd0c16340ceb32ffe811d6e88d10e40.png)](https://hackaday.com/wp-content/uploads/2016/10/nano32_3.jpg) 从外观上看， [Gravitech 和 Maker Asia](http://www.gravitech.us/naiotdebo4mb.html) 把 Espressif 的演示板和模块拆开，重新组装在一块 PCB 上。这意味着他们能够生产主板，而不会受到模块可用性的限制。Nano32 目前正在泰国生产，所以我们不知道他们需要多长时间才能到达你那里。

在美国， [Sparkfun](https://www.sparkfun.com/products/13907) 已经带着他们刚刚缺货的 ESP32 进入了拳击场。你应该收藏他们非常好的[入门指南](https://learn.sparkfun.com/tutorials/esp32-thing-hookup-guide)。他们对基本电路板的改动是增加了一个 LiPo 电池充电器。我们还不能对芯片进行功率测试，但 Espressif 的人员表示，他们已经在固件中添加了一些节能技巧，因此电池驱动的 WiFi 解决方案有望不远了。

在欧洲， [Pycom](https://www.pycom.io/webshop/) 有两种主板现在明显有货，并且都附带了他们的 MicroPython 固件。他们的 WiPy 2.0 与其他主板并没有太大的不同，但 [LoPy](https://www.pycom.io/product/lopy/) 是独特的，将 LoRa 无线电与 ESP32 配对，以一个半的价格为你提供三种无线电协议。如果你需要一个洛拉桥，或者你现在需要一个 ESP32，看看这些人。

[![](img/50d92e97b581e4bec5c3ada9dd81610e.png)](https://hackaday.com/wipyside-copy-510x510/)

Pycom’s WiPy

[![](img/d4f9945073ef6095188bb920d6460865.png)](https://hackaday.com/13907-01/)

Sparkfun’s ESP32 Thing

[![](img/2be60d2bbadaf75a47db180c520356cf.png)](https://hackaday.com/cvvxmgavmaa-vla/)

A Wildcard: the [ESPea32](http://wiki.aprbrother.com/wiki/ESPea32), aimed at the Internet of Gardening

还有很多其他的开发板，或者至少是设计。点击[ESP32.net](http://esp32.net/)并向下滚动到页面底部查看列表。如果你们中的任何人手中有这样的一个，或者是其中一个的开发者，请在评论中告诉我们。

## 模块

[![cwdi6eiviaa3lcu_thumbnail](img/7b5a3ef58e7c8e16e304ffe133bfbf2e.png)](https://hackaday.com/wp-content/uploads/2016/10/cwdi6eiviaa3lcu_thumbnail.png) 

ESP32S 坐在 ESP-WROOM32 上面。绝配！(Via [Angus Gratton])

如果你买了一个裸露的 ESP-XX 模块(ESP-01、ESP-07、ESP-12S……)，它很有可能是由[人工智能思考者](http://www.ai-thinker.com/)制造的。这是一个完全不科学的调查，但是他们占了我们在网上购买的裸模块样本的 100%。

据 Espressif 的[Angus Gratton]称，他们最早的 ESP32 模块草案被称为 ESP3212，已被废弃，代之以 ESP-32S，其引脚排列与 Espressif 的 WROOM32 相同。AI-Thinker 在 10 月初开始生产，在 Taobao.com 上有大约 8 美元[的模块。](https://world.taobao.com/item/540741221727.htm?spm=a312a.7700714.0.0.At55K3#detail)

我们很高兴看到模块的第二个来源，因为所有的缺货和延期交货都有点过时了。让我们加倍兴奋的是，他们使用了和 Espressif 一样的足迹。这是我们不用担心的另一件事。

## 摘要

目前谁有什么库存还在不断变化，但如果你看得更深一点，你可以找到一个 ESP32 开发板或模块。这一切在接下来的几周内肯定会改变，所以让我们知道你找到了什么，在哪里，多少钱。我们期待这些模块和开发板像它们的前辈一样无处不在，易于使用。