# NixieBot 拍摄你的推文

> 原文：<https://hackaday.com/2016/12/01/nixiebot-films-your-tweets/>

[Robin Bussell]的[nixie bot](https://hackaday.io/project/9155-nixiebot)是新时代电子产品和复古元件的混合体，他让一群黑客挤在里面。这是一个 Nixie tube 时钟，它可以显示推文，当它遇到带有#NixieBotShowMe 哈希标签的推文时，会对显示器拍照，然后将请求的图片发回到 twitter。如果一个单词有八个字符，它会进行快照。如果是更长的消息，NixieBot 会对每个单词拍摄一系列图片，将其转换为动画 GIF，然后发布推文。在此期间，它每 20 秒显示一次随机推文。你可以在下面的图片中看到相机的设置，你应该查看一下 [@nixiebot](https://twitter.com/NixieBot) twitter 上的一些动作。

为了这次展示，他使用了八个大的老式巴勒斯 B7971 谢妮电子管。这些不容易找到，如果你能找到的话，目前的价格在 100 美元左右。运行每个电子管所需的 170 伏 DC 来自一组六个 [12V 到 170 伏转换板](http://www.tayloredge.com/storefront/SmartNixie/PSU/index.html)，专门设计用于驱动这些电子管。每块板至少可以驱动几个 nixies，所以[Robin]可以用四块板来驱动八个电子管。每个谢妮都由自己的“ [B7971 SmartSocket](http://tayloredge.com/reference/Circuits/1386SmartSocket/index.html) 驱动，这是一个专门为该目的定制的专用 PIC16F690 微控制器板。串行协议可以轻松地将智能插座以菊花链形式连接起来，构建多字符显示器。

其余的构建相当简单。运行 Twython 的 Raspberry-Pi 用于 Twitter 通信，GrafixMagick 用于 GIF 创建，Picamera 用于拍照，GPIO 库用于控制显示。运行所有这些的软件都存放在他的 [GitHub 库](https://github.com/Zedsquared/NixieBot)上，上面有一些关于如何将它们组合在一起的基本说明。

更详细的参考资料可以在 [NixieBot 博客](http://nixiebot.tumblr.com/)上找到。他设计了一个 Pi 屏蔽板来容纳高压模块、5V DC-DC 转换器和 Pi GPIO 接头。他可能还有几个备用的，所以如果运气好能找到难以捉摸的谢妮电子管，再加上一些财力雄厚的人，建造你的 NixieBot 应该相对容易。

如果数码管机器人激起了你的兴趣，可以看看“[制作数码管的艺术](http://hackaday.com/2016/10/04/the-art-of-making-a-nixie-tube/)”，里面有[Dalibor Farnby]的作品。