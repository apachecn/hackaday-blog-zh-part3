# Seeed Studio 的 ReSpeaker 会说所有的语音识别语言

> 原文：<https://hackaday.com/2016/08/25/seeed-studios-respeaker-speaks-all-the-voice-recognition-languages/>

Seeed Studio 最近推出了第三次 Kickstarter 活动: [ReSpeaker，一个开放的硬件语音接口](https://www.kickstarter.com/projects/seeed/respeaker-an-open-modular-voice-interface-to-hack)。在他们之前启动的物联网硬件，如 RePhone，主要专注于连接性之后，这家来自深圳的电子制造商现在开始处理另一个竞争激烈的物联网领域:语音识别。

ReSpeaker 内核是一款基于联发科 MT7688 WiFi 模块的功能强大的开发板，运行 OpenWrt。板载 WM8960 立体声音频编解码器，集成 1W 扬声器/耳机驱动器、麦克风、ATMega32U4 协处理器、12 个可寻址 RGB LEDs 和 8 个触摸传感器。还有两个带有 GPIOs、I2S、I2C、模拟音频和 USB 2.0 的扩展接头和一个板载 microSD 卡插槽。

后者特别有助于为 ReSpeaker 的集成语音识别引擎 PocketSphinx 提供词汇和音频文件库，使其即使在没有连接到互联网的情况下也能对关键词和命令做出响应。一旦上线，ReSpeaker 还支持大多数可用的基于云的*认知*语音识别服务，如微软认知服务、亚马逊 Alexa 语音服务、谷歌语音 API、Wit.ai 和 Houndify。它还配有 SDK 和 Python API，支持 JavaScript、Lua 和 C/C++，看起来协处理器具有 Arduino 兼容的引导加载程序。

 [![respeaker_addons](img/e2e3d77ee3c1d0f770882693a58f8c64.png "respeaker_addons")](https://hackaday.com/2016/08/25/seeed-studios-respeaker-speaks-all-the-voice-recognition-languages/respeaker_addons-3/)  [![respeaker_micarray](img/878f76207f4fd332b59b834c7135f2d7.png "respeaker_micarray")](https://hackaday.com/2016/08/25/seeed-studios-respeaker-speaks-all-the-voice-recognition-languages/respeaker_micarray-2/) 

扩展接头接受盾状硬件附件。其中一些也可以通过活动获得。最重要的是圆形远场麦克风阵列。基于 7 XVSM-2000 [![respeaker_meow2](img/844c0b0a75f53dfcf13633c30f9819d7.png)](https://hackaday.com/wp-content/uploads/2016/08/respeaker_meow22.jpg) 数字麦克风，扩展板通过声音定位、波束形成、混响和噪声抑制来增强设备的听觉。Grove 扩展板将 ReSpeaker 连接到 Seeed 现有的即用型传感器、执行器和其他外围设备。

Seeed 还与喵王音频电子公司合作，开发了一个漂亮的塔形外壳，内置扬声器，5W 放大器和电池。作为一个便携式扬声器，*喵王驱动单元*(显示在右边)当然不会让你大吃一惊，但它实际上把 ReSpeaker 变成了亚马逊 Echo 的开源版本——包括离线运行的能力，而不是把你说的一切都传输给老大哥。

根据 Seeed 的说法，新出炉的硬件将于 2016 年 11 月交付给支持者，他们确实有按时交付 Kickstarter 奖励的记录。在撰写本文时，一些疯狂的早期用户仍然可以以 39 美元的价格买到。请欣赏下面的活动视频，并在评论中告诉我们您对 think hardware 的看法！

 [https://www.youtube.com/embed/a1SFoV7A26Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/a1SFoV7A26Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

