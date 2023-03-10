# 有没有从苹果买过音乐？用 Linux？你需要这个工具

> 原文：<https://hackaday.com/2016/07/21/ever-buy-music-from-apple-use-linux-you-need-this-tool/>

当然，你是一个铁杆超级用户，但这并不意味着你不享受生活中更美好的事情——比如闪亮的小松鼠和第一时间获得每个新应用。但是，像你这样不在乎操作系统的人在购买音乐的时候会怎么做呢？这就是 [recover_itunes 工具](https://github.com/kluete/recover_itunes)大放异彩的地方，如果你是一个拥有 iPhone 的 Linux 用户，它可能只是你新的最好的朋友。

当您从 iTunes 购买音乐时，iPhones 和其他苹果产品非常好用，但当您的音乐来自其他来源时，可能会令人头疼。另一方面，众所周知，从 iTunes 上购买的音乐很难在苹果产品以外的其他产品上听。后者困难的一个主要原因是 iTunes 处理元数据的方式。

出于某种偶然的奇迹，或者纯粹的意愿，我们的音乐库——以及我们用来收听它们的所有程序——大多坚持在音乐文件本身中保存元数据的标准；艺术家、专辑和歌名等重要内容的元数据。不幸的是，“大部分”不包括苹果。苹果使用一个包含所有信息的单独文件。

那么，知道了所有这些，当你把你的 iTunes 库复制到你的 Linux PC 上会发生什么呢？你会留下一些没有任何有用信息的文件。你所能做的就是用洗牌按钮玩俄罗斯轮盘，就像是在 90 年代，你在你的随身听上按了随机键。除了现在你有 5000 首歌曲可以跳过来找到“MMMBop”，而不是 CD 上的 21 首(说真的，[看看](https://en.wikipedia.org/wiki/Middle_of_Nowhere_(album))，那张 CD 上有 8 首无声的歌曲)。为什么不用一个长的无声音轨呢？)

由[kluete]创建的 [recover_itunes](https://github.com/kluete/recover_itunes) 程序解决了这个问题，用户几乎不用付出任何努力。将它指向你的音乐目录，它会搜索 iTunes 元数据以匹配任何 M4A 文件，保存插入元数据的文件副本。作为奖励，它甚至会试图找到匹配的专辑插图，这些插图在你一直打算建造的 HTPC[上看起来应该很棒。](https://hackaday.com/2015/11/22/control-your-htpc-with-scavenged-ir-parts/)

[感谢彼得]