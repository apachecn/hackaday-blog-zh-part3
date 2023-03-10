# 苹果手表上的 Windows 95

> 原文：<https://hackaday.com/2016/04/30/windows-95-on-an-apple-watch/>

如果你的 Apple Watch 光滑的用户界面和紧密的 iOS 集成让你想要更多，会发生什么？一个真正的操作系统，从男人是 T2 男人和电脑是灰色大盒子的时代开始！

[尼克·李]用他的手表[解决了这个意想不到的问题，他得到了一个可以在它上面运行的 Windows 95 的工作副本](https://medium.com/tendigi-insights/i-installed-windows-95-on-my-apple-watch-589fda5e36d)。理论上，它应该一点也不难，520 MHz 的 ARM，512 MB 的 RAM 和 8GB 的存储空间，你可能会认为它会让我们当年轻松运行的快速 486 和低端奔腾黯然失色。但当然，在手表上运行旧的 Redmond 操作系统的能力可能不是苹果开发团队的首要功能，所以[Nick]必须经历相当多的磨难才能实现它。

正如你所料，95 年的安装并没有直接在手表上运行。在没有 x86 处理器的情况下，他的复杂开发过程包括让 Bochs x86 仿真器为手表编译，然后给它一个 95 年的镜像来启动。结果是滑稽的慢，一个小时的开机时间和一个连接到手表的小电机振动它，阻止它进入睡眠。这无论如何都不是一个有用的练习，毕竟谁会真的想在手表上使用 95 年的时间呢？Internet Explorer 3 和微软网络，多么方便！但这是一种“因为你能”的练习，我们为(尼克)让它发生而鼓掌。如果你想试一试，[他的 Bochs-forWatchOS 代码在 Github](https://github.com/nickplee/BochsWatchOS) 上。

广告下方的视频显示了启动 95 手表、打开开始菜单和运行其中一个纸牌游戏的过程。人们几乎可以感觉到外面不断拉长的影子。

 [https://www.youtube.com/embed/Nas7hQQHDLs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Nas7hQQHDLs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



在我们的社区中似乎有一种奇怪的吸引力，让 Windows 95 在意想不到的设备上运行。我们记得在 2012 年看到人们在当时刚刚推出的 Raspberry Pi 上这样做，在 Hackaday 上，我们特别介绍了在诺基亚 N 系列塞班手机和[GP2X 游戏机](http://hackaday.com/2006/01/28/windows-95-on-a-gp2x/)上运行的[。有些人会做任何事情来听到窗户的声音。](http://hackaday.com/2009/02/24/windows-95-running-on-an-n95/)