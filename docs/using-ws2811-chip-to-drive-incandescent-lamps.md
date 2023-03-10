# 用 WS2811 芯片驱动白炽灯

> 原文：<https://hackaday.com/2016/06/12/using-ws2811-chip-to-drive-incandescent-lamps/>

是什么让 WS2812 风格的可单独寻址像素 led 如此诱人？他们丰富的色彩？不，你可以在任何地方得到 RGB 发光二极管。他们的外形？没有。即使是表面贴装 RGB 也很丰富和便宜。答案是:它是集成控制器。对你的 led 说一个类似 SPI 的协议是如此方便——它将电源和数据分开，你可以根据自己的需要将它们链接起来。将该控制器和 led 组合在一个封装中，您就获得了巨大的产品成功。

但在 WS2812 之前，有 ws 2811——一个独立的 RGB 控制器 IC。随着 ws 2812 上市，没有人再想要低端的 WS2811 了。也就是说，除了(迈克尔·克鲁姆普斯)没有人。你看，他喜欢老式的白炽灯光，但喜欢 WS2812 灯串易于驱动和延伸的方式。于是他买了一包 ws 2811s[把两个放在一起](http://nootropicdesign.com/projectlab/2016/05/21/individually-addressable-incandescent-lamps/)。

控制器 IC 无法处理白炽灯泡所需的电流，因此他添加了一个 MOSFET 来完成繁重的工作。在将这些单元连接在一起后，他发现(正如人们最终对基于 LED 的 WS2812s 所做的那样)开关瞬态可以拉低电源线，因此每个灯泡都有一个强大的电容器。

他希望每个灯泡都可以独立寻址，所以他只使用了 RGB 控制器的蓝线，这使得两个输出为空。我相信你能想出办法解决它们。

不用说，我们已经在这里看到了很多 WS2812 黑客。很难挑一个最喜欢的。因“迈克的电动工具”而出名的[迈克]建造了可能是我们见过的最大的装置，这个黑客有效地将[投影映射到 WS2812s 的随机放置的字符串](http://hackaday.com/2015/12/30/must-have-overkill-christmas-tree-lights/)上，这非常酷。但老实说，没有一个闪烁或发光的项目会出错，对吗？

 [https://www.youtube.com/embed/KKqlYEkFE3k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/KKqlYEkFE3k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

