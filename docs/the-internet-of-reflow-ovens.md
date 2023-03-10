# 回流炉的互联网

> 原文：<https://hackaday.com/2015/11/28/the-internet-of-reflow-ovens/>

使用烤面包机回流焊料并不是一个新想法。但是[Sukasa]想要有更多功能和更好的外观的东西。所以他结合了一个 Netduino、一个烤面包机和一些固态继电器来制造一个看起来干净的回流焊炉。他的目标是不要让不经意的观察者看到任何明显的修改。然而，烤箱内部现在有一个网络连接，可以通过网络浏览器或 JSON 查看系统状态。

烤箱的新大脑是一个 Netduino Plus 2 和一个 I2C 端口扩展器，它可以连接到一些额外的 I/O 设备。然而，具有挑战性的 I/O 是加热器。冷的时候，烤箱可以消耗超过 16 安培的电流，所以一对 12A 的固态继电器~~并联~~来处理这个负载。还有两个风扇:一个用于保持电子设备冷却，另一个用于软件控制。IGBT 允许控制器对风扇的输出进行脉宽调制。一对 MAX31855s 读取报告温度的热电偶。

控制器是现有烤箱键盘和附加液晶显示器的混搭(见右图)。我们没看到的是一张示意图。当然，你可以阅读代码并弄清楚它们是如何连接的，而且(除非你使用完全相同的烤箱)你可能需要修改一些东西来适应你的特殊设置。

我们过去已经见过其他好看的回流焊炉[和控制器](http://hackaday.com/2015/07/15/android-based-reflow-brings-solder-profiles-to-your-lab/)，包括一个带触摸屏的。同样值得注意的是，如果你不想自己卷，你现在可以找到价格相对较低的回流焊炉。