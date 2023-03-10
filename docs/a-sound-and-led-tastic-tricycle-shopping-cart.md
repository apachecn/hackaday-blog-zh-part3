# 一个声音和 LED-tastic 三轮车购物车

> 原文：<https://hackaday.com/2015/12/05/a-sound-and-led-tastic-tricycle-shopping-cart/>

当你把大量的发光二极管与购物车和自行车组合在一起时，你会得到什么？一辆由[kramerr]设计的超赞的 rave-mobile。他甚至更进一步，让电子设备由太阳能供电。

[Kramerr]通过多个 WS2803 LED 驱动器控制 LED。三个 pic 18 f 4550 通过 SPI 控制 WS2803s。他设计了一种从音乐中激发发光二极管的巧妙方法，使用一对图形均衡器显示滤波器芯片 MSGEQ7s 来驱动 PICs 创建图案。USB 输入也允许图片显示歌曲名称或其他信息。

![leds and boards](img/abe3e752671826511a77070bd8d7cb6e.png)

机械设计和电子设备一样令人印象深刻。自行车的后半部分焊接在购物车的框架上，购物车的把手用于转向。购物车的后轮被小自行车车轮取代。

但是[Kramerr]还没有完成。由于找不到符合尺寸要求的太阳能电池板，他自己做了一块。该电池板由 26 个串联的电池组成，在晴天以 13V 的电压提供 1A。太阳能充电控制器保持标准的 12v 铅酸电池随时为三轮车提供动力。

而且还有更多！有一个树莓皮驱动的音响系统。当[Krameer]想要显示歌曲名称或艺术家而不是音频模式时，Pi 也驱动 USB 输入。

在这个项目中，至少有四个方面值得称赞。[Karmeer]在一个项目中完成了所有这些，值得称赞。如果你正在寻找不那么炫目的*和不那么踩踏板的*，我们可以向你推荐[这款电动、骑行购物车](http://hackaday.com/2013/12/17/shopping-trolley-is-wired-for-camp/)。

休息之后，通过视频播放一些狂欢音乐和灯光。

 [https://www.youtube.com/embed/XhKE1ltqUc8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XhKE1ltqUc8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

