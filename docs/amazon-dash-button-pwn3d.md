# 亚马逊破折号按钮 Pwn3d

> 原文：<https://hackaday.com/2015/12/02/amazon-dash-button-pwn3d/>

如果你还没有听说过亚马逊 dash 按钮，我们很高兴你停止观看猫视频并加入我们。只是为了让你跟上速度:亚马逊 dash 按钮是一个小的无线设备，让你的懒屁股通过按下“dash 按钮”订购更多的洗衣皂，这个按钮应该贴在你洗衣机附近的东西上。按下按钮将启动我们过去所知的“购买我们用完的东西”的痛苦过程，但多亏了亚马逊，我们现在可以用各种各样的按钮覆盖我们的整个生活，不需要任何凭证来实际推动。我们不认为这有什么问题。

不用说，作为一个团体，我们开始为这些神奇的小设备寻找实际用途。[maximus64] [在以最可用的方式启用硬件方面做得相当不错](https://github.com/maximus64/amazon-dash-wiced)。我们看到的大多数针对 dash 按钮的黑客都删除了物理按钮，并添加了某种传感器。用传感器替换按钮仍然使用 WiFi 连接将数据从按钮发送到云端。取代从亚马逊订购更多`<<产品>>`的按钮，传感器可能会触发 dash 来增加你网站上的计数器，让你知道你的狗穿过狗门+1 次。

[maximus64]通过将 Broadcom IoT WICED SDK 移植到按钮上，使 dash 按钮以相反的方式工作。他用 dash 按钮作为接收器，当[maximus64]从他的笔记本电脑向 dash 按钮发送“一切正常”信号时，他的车库门打开了，你可以在休息后的视频中看到。我们发现这比破折号按钮的原始用途更加有用。[maximus64]在 github repo 的 readme.md 文件中有说明，所以你也可以用这种方法破解你的 dash 按钮。

我们已经看到了相当多的亚马逊 dash 按钮黑客，包括[maximus64]对我们要求您分享您的概念证明以控制 dash 按钮中的 WiFi 模块的响应。

 [https://www.youtube.com/embed/6wzxGu91c1I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6wzxGu91c1I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

