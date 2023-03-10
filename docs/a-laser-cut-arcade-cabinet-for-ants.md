# 蚂蚁激光切割拱廊橱柜

> 原文：<https://hackaday.com/2017/12/25/a-laser-cut-arcade-cabinet-for-ants/>

我们大多数人可能喜欢在家里有一个拱廊橱柜，但很难证明它们占用的空间是合理的。当然，当朋友聚会时，这是一个非常棒的对话开始，你甚至可以定期播放它，但在某些时候，你会看向角落，意识到你可能可以在房间的特定区域做一些更实际的事情。

也许解决的办法就是做一个小一点的。你可以做一半大小的，甚至是桌面大小的。但是为什么就此打住呢？为什么不把它做得很小，当你不需要的时候可以把它放在抽屉里呢？虽然这可能更像是一个学术实验，而不是一个实用的娱乐设备， [[RedPixel]已经成功地用 Pi Zero 和激光切割木材](https://pixel.red/project/tiny-arcade/)创造了这样一个易于隐藏的街机橱柜。只有 83 毫米高，这可能是有史以来最小的功能性街机柜(至少现在是这样)。

[![](img/c64082553e05f46ee489ee08e2d206c3.png)](https://hackaday.com/wp-content/uploads/2017/12/antcade_feat_thumbnail.png) 所有的橱柜部件都是用 3 毫米厚的胶合板绘制而成。按钮和操纵杆直接连接到 Pi Zero 的 GPIO 引脚，并配置有 [Adafruit-retrogame](https://github.com/adafruit/Adafruit-Retrogame) 。显示器是 SPI ILI9163，这是 [[RedPixel]之前在他的网站](https://pixel.red/guide/ili9163-screen-on-retropie/)上记录的。

Pi 运行的是一直很受欢迎的 RetroPie，它允许这个小小的街机柜模拟 1000 个控制台和街机游戏，假设你能处理好控制。虽然[RedPixel]上传了一段他的小人国柜子运行模拟器的视频，但没有他实际玩这个东西的视频。虽然我们不怀疑它的功能，但在如此小的输入阵列上玩游戏肯定非常困难。

这可能是迄今为止最小的功能性街机机柜，[但它也不是没有挑战者](https://hackaday.com/2015/11/21/tiny-arcade-based-on-arduino/)。[我们已经介绍了一些非常令人印象深刻的构建](https://hackaday.com/2012/12/11/building-a-tiny-arcade-cabinet-from-a-game-boy-advance/)，它们设法调用庞大的硬币模型[的外观和感觉，尽管它们可以整齐地放在你的桌子上](https://hackaday.com/2014/11/04/a-tiny-arcade-machine-with-tinier-buttons/)。

 [https://www.youtube.com/embed/WmS9Bi0GHno?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/WmS9Bi0GHno?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

