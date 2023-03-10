# 不可能的任务:渗透弗比

> 原文：<https://hackaday.com/2017/11/26/mission-impossible-infiltrating-furby/>

早在这些东西“像病毒一样传播”之前，每年总有一些“必须拥有”的玩具需求量很大。卷心菜娃娃、变形金刚或泰迪熊会让父母们歇斯底里地想要得到一个玩具作为节日礼物。1998 年，这种玩具是 Furby——一种会说话的机器人宠物。你仍然可以购买 Furby，正如你所料，一个现代的 Furby Connect 可以上网，比以前的版本更智能。虽然 Furby 一直是优秀黑客攻击的目标，但任何支持互联网的东西也可能成为恶意黑客攻击的目标。[上下文信息安全]决定看看他们能否[控制你孩子的机器宠物](https://www.contextis.com/blog/dont-feed-them-after-midnight-reverse-engineering-the-furby-connect)。

Thet Furby Connect 的互联网路径是通过 BLE 到一个配套的电话设备。反过来，这款手机会与孩之宝(玩具制造商)的亚马逊网络服务服务器进行对话。该公司推出新的歌曲、游戏和舞蹈。因为 BLE 很慢，在正常的玩具操作过程中，传输发生在后台。

看看 BLE 服务，有一个上传固件的通用 DFU 服务和一个发送专有 DLC 文件的接口。他们发现了一个现有的项目，可以将现有的 DLC 文件发送到设备上，甚至可以替换这些文件中的音频。然而，在 Hasbro 之外，DLC 文件的格式似乎是未知的。

用十六进制编辑器攻击 DLC 文件，有些看起来很明显。然而，其中一些很难理解。这篇文章详细描述了这次调查，正如你在下面的视频中看到的，他们成功了。

孩之宝似乎并不太担心安全问题，因为攻击者必须靠近玩具。不难想到这不是一个很好的借口，但我们认为它确实涵盖了你担心的最常见的事情。

我们之前讨论过 Furby Connect 的[部分漏洞。如果你的阁楼里有一只老 Furby，你可以随时](https://hackaday.com/2017/01/21/taking-control-of-your-furby/)[把它变成你的下一个机器人](https://hackaday.com/2016/01/29/open-furby-opens-the-furby/)。

 [https://www.youtube.com/embed/h2DY-VCtb54?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/h2DY-VCtb54?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

