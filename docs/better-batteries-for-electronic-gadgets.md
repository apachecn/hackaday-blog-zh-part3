# 更好的电子产品电池

> 原文：<https://hackaday.com/2015/09/06/better-batteries-for-electronic-gadgets/>

我们不再使用 9 伏电池为我们的项目供电；爱好电子产品的世界已经转移到我们大多数移动电源存储的廉价脂肪电池。抽脂并不是最好的解决方案，YouTube 上数百个电池爆炸的视频，以及我们的垃圾抽屉里不止几个膨胀的电池都证明了这一点。解决办法？磷酸铁锂电池。它们是一种更安全的化学物质，自放电低，比其他化学物质的锂电池更容易充电。

不过，如果你在用试验板电子设备工作，磷酸铁锂电池就不容易处理了。这主要是因为这些单元没有多少分线板。[Patrick]正在努力用他的 life po 4 word USB 充电器来改变这种情况。

这个概念很简单:使用现成的 LiFePO4 电池部件——在这种情况下是一个[MCP 73123](http://www.microchip.com/wwwproducts/Devices.aspx?product=MCP73123)——并制作一个带 USB 端口的电池充电板。这与许多 USB LiPo 充电器的想法完全相同，只是这款使用了更好的电池化学物质。

[Patrick]在这个项目中使用了 550 毫安时的电池，但没有理由不能升级到 18650 大小的电池，内部填充 2000 毫安时以上的电池。在电路中添加一个升压转换器，他将拥有一个完美的电源，可以用于任何可以想象的便携式电子项目。