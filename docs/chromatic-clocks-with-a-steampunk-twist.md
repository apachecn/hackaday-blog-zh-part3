# 蒸汽朋克风格的彩色时钟

> 原文：<https://hackaday.com/2015/12/04/chromatic-clocks-with-a-steampunk-twist/>

没有什么比一个好的时钟项目更好的了，加上蒸汽朋克修改器只会让它变得更好。[José]建造了一个蒸汽朋克钟，它比仅仅在外壳上粘上一些齿轮，然后称之为一天要好得多。这个造型包括用不同颜色显示时间的发光珠宝，同时展示了蒸汽轮机手使用切管器的高超技艺。

时钟的主体是一块上漆的木头，隐藏着一个带 DS3231 实时时钟的 perfboard 结构，一个 DHT22 温度和湿度传感器，以及一个根据环境光水平调节 WS2812 LEDs 的光传感器。

时钟的其余部分是一堆 12 毫米的铜管，弯头，和 t 型耦合器。这些管道的末端用大理石盖住，时钟的每个“数字”后面都有 RGB 发光二极管。这是一个彩色时钟，根据电阻颜色编码方案，数字 0 到 9 被指定为不同的颜色，黑色和棕色除外。一旦你知道了如何用这个时钟报时，在你的垃圾箱里找到那个 56k 电阻应该没有问题。

你可以看看下面这个时钟的视频。

 [https://www.youtube.com/embed/4V6ATqfs6JM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/4V6ATqfs6JM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

