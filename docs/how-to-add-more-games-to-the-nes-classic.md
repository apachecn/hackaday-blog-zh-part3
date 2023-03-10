# 如何在 NES 经典游戏中加入更多游戏

> 原文：<https://hackaday.com/2017/01/10/how-to-add-more-games-to-the-nes-classic/>

围绕 2016 年 NES 经典赛的炒作是巨大的，正如预期的那样，单元已经在易贝以过高的价格出售。这款游戏机预装了 30 款游戏，主要是任天堂第一方发布的游戏。但是不用担心，现在有一种方法可以给你的 NES 经典游戏添加更多的游戏！

像许多好的黑客一样，这一个起源于一个论坛社区。[【mad monkey】在 GBX.ru](http://gbx.ru/?showtopic=115261&st=440) 上发帖讲述了他们试图在主机上加载额外游戏的行为。第一步是使用 Allwinner SOC 的引导 ROM 的 FEL 子例程来转储单元的闪存。从那里，它是一个使用定制工具注入额外的游戏 rom，然后重新燃烧修改后的图像到控制台的问题。最初使用的工具名为 hakchi，需要将超级马里奥储蓄游戏放入特定的插槽才能正常工作，尽管新版本已经出现，取消了这一要求。

虽然这只是一个软件修改，但它确实会带来一些风险。除了阻止您的控制台，病毒扫描程序还报告这些工具具有潜在的危险。对于这些是否是误报，社区中存在混乱。就像你在论坛上发现的任何东西一样，你的收获可能会有所不同。但是如果你不得不第无数次打败 Battletoads，加载一个 VM 进行安装并开始安装。这个 Reddit 主题(从[最初的 pastebin 指令](http://pastebin.com/af2RxZ6z)扩展而来)对于勇敢者来说是一个很好的起点。

发布仅几个月，NES 经典就已经成为黑客的沃土——去年我们报道了[这个控制器模块](http://hackaday.com/2016/12/29/nes-classic-edition-controller-mod/)和[如何安装 Linux](http://hackaday.com/2016/11/13/linux-on-your-nes-classic-edition/) 。视频这 ROM 注入黑客休息后。

 [https://www.youtube.com/embed/BF-0nAddPZQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/BF-0nAddPZQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

