# 另一种电话窃听

> 原文：<https://hackaday.com/2017/06/06/the-other-kind-of-phone-hacking/>

虽然你的零件箱可能会有一些从最近几年的过时设备中收集的零件，但除了壁瘤之外，没有太多可以收集的了。但是来自[Kerry Wong]的旧 Uniden 无绳固定电话的 3×48 字符 LCD 足够吸引他去尝试[拆卸和逆向工程](http://www.kerrywong.com/2017/06/04/reverse-engineering-a-uniden-cordlessphone-lcd/)，并且结果是有指导意义的。

没有数据表？没问题。[Kerry]找不到任何关于漂亮背光显示器的信息，所以转到了逻辑分析仪上。从主板到显示模块只有八根导线，这不太可能是并行协议，下面的视频显示了这种情况。稍微修改一下参数就可以看出该协议是串行外设接口，但是和其他没有完全标准化的标准一样，[Kerry]留下了足够的模糊性，使得分析变得有趣。尽管有一个 39 个字符的神秘标题，但他最终能够用 Arduino 驱动 LCD，并且考虑到这些手机通常与一个底座和几个手机捆绑销售，他应该有一个不错的零件箱显示器收藏。

随着这种协议变得如此流行，[Kerry]的帖子让我们想要[了解 SPI 的基础知识](http://hackaday.com/2016/07/01/what-could-go-wrong-spi/)。并且给[也买一个逻辑分析仪](http://hackaday.com/2015/05/26/review-dslogic-logic-analyzer/)。

 [https://www.youtube.com/embed/pbEq4s9UKbo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/pbEq4s9UKbo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

