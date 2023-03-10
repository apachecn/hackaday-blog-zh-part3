# 简单的扫描仪找到最好的 WiFi 信号

> 原文：<https://hackaday.com/2017/04/21/simple-scanner-finds-the-best-wifi-signal/>

想知道您的 WiFi 天线指向哪个方向才能获得最佳信号？对于我们大多数人来说，这是一个猜谜游戏，但是使用大多数现成的组件快速构建一个扫描 WiFi 天线可以为你指明正确的方向。

如今，在大多数地方 WiFi 覆盖饱和的情况下，优化你的信号似乎是一项毫无意义的工作。的确，看起来[shawnhymel]建造这个更多的是为了好玩，而不是为了实用。尽管如此，我们还是可以看到扫描八木天线派上用场的应用。构建从一个简单的家酿八木-Uda 和一个 ESP8266 创建的“WiFi 占卜棒”[shawnhymel]开始，以显示来自特定接入点的接收信号强度指示(RSSI)。厌倦了手动移动冰棒棒和回形针天线，他建造了一个双轴扫描仪，通过完整的半球摆动天线。

每个点的 RSSI 都会被记录下来，当扫描完成后，天线会摆回到最强的点。考虑到天线不太完美的方向性——[shawnhymel]以窄波束宽度换取增益——我们认为“最强点”有些主观，但如果有一个更好的天线，这可能是一个方便的工具，用于现场勘测、自动无线电测向，或者只是绘制您附近的射频环境。

八木宇田天线和 WiFi 并不陌生，无论是[一把 WiFi 狙击枪](http://hackaday.com/2016/10/15/a-lot-of-wifi-power-a-yagi-and-a-snipers-scope/)还是[另一个回收站八木](http://hackaday.com/2017/01/24/a-simple-yagi-antenna-for-your-wi-fi-router/)。当然，这款扫描仪不仅限于 WiFi。也许扫描[2 米波段的轻型八木](http://hackaday.com/2017/02/13/a-lightweight-two-metre-carbon-fibre-yagi-antenna/)将是锁定当地火腿中继器的好方法。

 [https://www.youtube.com/embed/LuKQTdas-W0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LuKQTdas-W0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

