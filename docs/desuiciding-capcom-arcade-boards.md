# 取消 Capcom 街机板

> 原文：<https://hackaday.com/2016/09/15/desuiciding-capcom-arcade-boards/>

卡普空的 CP S2——或 CP System II——是 90 年代早期至中期的街机硬件，因《超级街头霸王 II》、《异形大战掠夺者》以及漫威和卡普空的几款跨界街机游戏而闻名。正如你所料，这些板已经成为收藏家的物品。对后代来说不幸的是，卡普空采取了一些短视的安全措施来防止复制游戏，而董事会在过去二十年里一直失败。

经过几个月的工作，【ArcadeHacker】和其他几个街机爱好者已经逆向设计了安全协议，[设计了一种去自杀这些街机板](http://arcadehacker.blogspot.mx/2016/09/capcom-cps2-security-programming-guide.html)的方法，允许保存这个硬件和这些游戏。实现这个功能的[代码](https://github.com/ArcadeHacker/ArcadeHacker_CPS2)在 GitHub 上。

去年，[ArcadeHacker]对 Capcom 的 Kabuki 处理器的片上安全性进行了逆向工程，该处理器用于 Capcom 早期的一些街机主板。它使用了类似的保护方案。在 Kabuki 硬件中，片上 ROM 与处理器总线上的几个异或门穿插在一起。由于安全密钥保存在电池支持的存储器中，这足以保持游戏代码的秘密，尽管代价是阻止历史保存。

在接下来的几周内，[ArcadeHacker]将会发布更多关于 CPS2 板的复制保护方案的详细信息，但是概念验证现在就可以工作。现在可以复活由于电池没电而自行死亡的 CPS2 板，硬件就像 Arduino 和几个测试剪辑一样简单。你可以看看下面的视频。

 [https://www.youtube.com/embed/ulIi9B74HMs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ulIi9B74HMs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

