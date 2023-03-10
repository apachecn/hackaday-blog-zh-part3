# 荒谬时钟使用 12 个 ESP8266 模块

> 原文：<https://hackaday.com/2015/11/26/absurd-overuse-of-esp8266-in-a-clock/>

快速测验:制作一个 LED 时钟需要多少个 ESP8266 模块？提示:时钟显示 12 小时。

没有。答案是*不是*12。但这并没有阻止 Hackaday.io 用户[tamberg]在西班牙毕尔巴鄂的创客节期间[制作了一个 12 秒钟](https://hackaday.io/project/8552-esp-clock)。使用这么多 ESP8266s 的“优势”是每个 ESP8266s 可以独立控制一个小时 LED 及其相关的五个分钟标记 LED。每个 ESP 通过互联网获取时间，但只有到时间时才会亮起。

就像并行处理什么的。或者它是多余的和安全的。也可能只是试图把最大限度的互联网化放到一个东西里。也许他们有一个 12 人的团队，想要平均分配负载。(我们想不出你想这么做的真正原因。)

抛开所有的风险不谈，这个项目看起来很棒，你可以在这个 Flickr 图库中看到[，如果你想重用这个项目的任何部分，所有的](https://www.flickr.com/photos/tamberg/sets/72157661456853951)[设计文件](http://www.thingiverse.com/thing:1134525)都是可用的。我们认为钟面很酷。

每个单元的代码可供您查阅。在第 13 行，您可以看到他们设置了一个变量(在固件中),告诉每个 ESP 它代表哪个小时。

更有趣的是，从第 38 行开始是一个从最近的 Google 服务器提取时间的小技巧。基本上，Goog 返回一个“Date:”字符串，代码读取它。在 ESP 论坛上阅读更多关于这项技术的内容。

评论员们，启动你们的“过度杀伤”激光器；我们喜欢这个项目，因为它做得对。至少不是一个[电锯供电的手电筒。](http://hackaday.com/2010/08/08/chainsawflashlight-overkill/)

[https://embedr.flickr.com/photos/22978920380](https://embedr.flickr.com/photos/22978920380)

[上面看到的 Flickr 视频](https://www.flickr.com/photos/tamberg/22978920380)有这样的描述:

> 每个 ESP 控制时钟的 5 分钟部分。启动时，没有连接(橙色)。一旦连接到 WiFi 网络(蓝色)，每个 ESP 通过一个简单的 HEAD Web 请求向 google.com 轮询当前时间，然后显示它所在的时钟部分(蓝色或粉色，绿色分钟)。请注意由片的独立操作引起的“故障”(加上片 0 中的一个编程错误，稍后修复)。红色按钮应该显示心跳并重置所有 esp，但没有足够的时间来实现这一点。对于这个视频，时钟显示秒，而不是分钟，就像完成的版本一样。