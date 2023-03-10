# 将路边的阴极射线管电视转换成街机显示器

> 原文：<https://hackaday.com/2018/05/30/convert-a-curbside-crt-tv-into-an-arcade-monitor/>

虽然一台旧的 CRT 电视可能在 MAME 橱柜项目中工作得足够好，但真正的街机纯粹主义者很快就会指出，一台合适的街机显示器和一台电视不是一回事。真正的街机板使用 RGB 连接到显示器，即直接控制红、绿、蓝信号。相反，同轴视频或复合视频，即大多数人联想到的老式 CRT 电视，将所有视频信息组合成一个模拟信号。简而言之，RGB 比合成图像更清晰。

许多在街机修复现场的人说，试图将 bog 标准 CRT 电视转换成 RGB 显示器是不可能的，但[街机杰森]有他的疑虑。在他的 YouTube 频道上，他最近发布了一个教程，讲述如何用相对较少的工作从一台废弃的 CRT 电视变成一台配得上街机游戏的显示器。随着真正的街机显示器变得越来越罕见，这种修改可能会变得更加普遍，因为投币游戏玩家希望保持旧的方式。

显然，每台电视的内部都将有所不同。所有的 CRT 电视都含有高电压，有些电路板甚至没有与电源隔离，所以如果你尝试这样做要小心。[Jason]当然，他并没有说他演示的方法可以在你碰巧看到的旧电视上工作。但是，他展示的总体思路和一些技术适用于大多数现代电视，可以帮助你根据自己的特定设备量身定制方法。一切都是从湿手指开始的。说真的。

[Jason]演示了一种非常独特的方法，通过将手指弄湿并在引脚上滑动，来确定电视控制芯片上的哪些引脚负责各个颜色信号。当在显示的图像上看到颜色的变化时，你知道你已经很接近了。我们不能说这是最科学甚至是最安全的方法，但对他来说很管用。

然后，他用跳线和电阻器找到负责每种颜色的精确引脚，并焊接街机板的实际 RGB 连接。除了三根彩色导线，还需要一个同步信号。这与复合视频中使用的同步信号相同，因此只需焊接到原始复合视频插孔的焊盘上。加上一个地面信号，你就有了一个合适的 RGB 显示器。

有趣的是，这一次又兜了一圈，正如[Jason]所说的那样[他的尝试是受到 Hackaday](https://hackaday.com/2013/06/17/modifying-a-crt-television-for-use-as-an-arcade-monitor/)上一篇旧帖子的启发。就是黑客生活的圈子。

[感谢 Seebach 的提示]

 [https://www.youtube.com/embed/MmiBhLUkKEM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MmiBhLUkKEM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

