# 带回 IPhone7 耳机插孔

> 原文：<https://hackaday.com/2017/09/07/bringing-back-the-iphone7-headphone-jack/>

许多人哀叹苹果选择在 iPhone 7 上取消 1/8”耳机插孔。[Scotty Allen]对此也不高兴，但他决定做点什么:[他设计了一个定制的柔性电路，并把插孔带了回来](http://strangeparts.com/bringing-back-the-iphone-headphone-jack-in-china/)。如果你认不出[Scotty]，他就是[用从深圳市场](https://hackaday.com/2017/04/13/defeat-the-markup-iphone-built-by-cruising-shenzhen/)获得的零件组装 iPhone 6 的那个人。这些相同的市场现在被用来设计和原型一个全新的电路。

iPhone 7 有一个气压通风口，正好位于 iPhone 6 的耳机插孔。透气产品有助于气压传感器获得准确的读数，同时保持手机防水。[Scotty]不担心防水问题，因为他在箱子上开了一个洞。通风口被去掉了，取而代之的是一个精心改造的耳机插孔。

下一步是说服手机播放模拟信号。为此，[Scotty]使用了苹果自己的耳机适配器的零件。困难的部分是使所有这些工作并保持 lightning 端口可用。关键是一个数字开关芯片。电路是这样工作的:

当没有耳机插入时，数据从 iPhone 的主板传送到 lightning 端口。当耳机插入时，数据线被切换到耳机适配器。不幸的是，这意味着手机不能同时播放音乐和充电——这是 2.0 版本的事情。

这个视频中的真正旅程是看着[Scotty]将所有这些部件装进 iPhone 外壳。该设计从试验板开始，经过原型印刷电路板的多次迭代。最终产品是使用柔性 PCB 制成的——琥珀色的 Kapton 和铜三明治，如今可以在每个移动设备中找到。

让一切都合适并不容易。两个 iPhone 屏幕在这个过程中消失了。但最终，[斯科特]成功了。他将自己的设计开源，这样世界就可以在此基础上进行构建和改进。

想了解更多关于 iPhone 7 和耳机插孔的信息吗？看看[这个点](https://hackaday.com/2016/07/15/ask-hackaday-does-apple-know-jack-about-headphones/)和[的对位法。](https://hackaday.com/2016/10/25/death-to-the-3-5mm-audio-jack-long-live-wireless/)我们发表了关于这个话题的文章。

 [https://www.youtube.com/embed/utfbE3_uAMA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/utfbE3_uAMA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

