# 游戏男孩颜色的 DIY 协处理器

> 原文：<https://hackaday.com/2016/11/09/diy-coprocessors-for-the-game-boy-color/>

回到过去，当视频游戏还在盒式磁带上时，制造这些手推车的工程师和程序员有很多选择。90 年代出现的最具创造性、最聪明、最有趣的墨盒之一是超级任天堂的星狐。 *Star Fox* 配备了一个协处理器芯片 Super FX，它实际上是一个用于在帧缓冲区中绘制多边形的 GPU。没有这个，*星狐*就不会是 3D，*耀西的岛*就不会那么可爱，你的电脑里就不会有一个永远在线的处理器有可能窥探你做的一切。

超级 FX 芯片、Capcom 开发的 Cx4 协处理器和任天堂 DSP 都生活在一个盒子里，但将更好的计算机放在盒子里的技术从未出现在任天堂的手持设备上。廉价、强大的微控制器现在随处可见，制作一个带卡边连接器的电路板并不困难，这让【安德斯】和[为游戏机颜色](http://www.happydaze.se/wolf/)构建了一个超级 FX。

Game Boy 墨盒很简单，只需要一个内存控制器和一些内存。加入一个微控制器，你就有了一个游戏机协处理器。该盒式磁带具有 MBC1 存储体控制器、512kB 闪存和 8KB SRAM。这些都是相当标准的器件，但该板还有最后一个诀窍:恩智浦的 KE04，一个运行在 48MHz 的 ARM Cortex-M0+微控制器。这个微控制器实际上是游戏机的 GPU。

这款基于 ARM 的协处理器能够在 2 毫秒内将帧缓冲区转换为图块，为系统提供充足的时间进行图像处理和渲染。由于 Game Boy 的限制，该协处理器提供的最佳分辨率为 160×96 或 128×128 像素，达不到 Game Boy 彩色的完整 160×144 像素显示屏。

即使[Anders]仍在致力于编程这个东西，以展示他的 Game Boy 协处理器的能力，他也有一些演示可以展示。最令人印象深刻的是一个类似沃尔芬斯坦的克隆体。这是非常令人印象深刻的和断然不可能的股票游戏男孩的颜色。

 [https://www.youtube.com/embed/Ro5VBl8i4OI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Ro5VBl8i4OI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/lk1NptFSYAQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lk1NptFSYAQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

