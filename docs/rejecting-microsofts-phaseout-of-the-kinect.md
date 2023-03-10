# 拒绝微软逐步淘汰 Kinect

> 原文：<https://hackaday.com/2018/02/18/rejecting-microsofts-phaseout-of-the-kinect/>

除非你了解最新的游戏硬件，否则你可能不会意识到，但微软正试图扼杀 Kinect。虽然 Xbox One 在发布时将其作为一个强制性的打包附件(后来为了降低成本而放弃了)，但最新版本的系统甚至没有专用端口来插入它。有一段时间，微软提供了一种适配器，可以让你将其插入到游戏机的 USB 端口之一，但现在甚至已经停止了。仍想使用 Kinect 的最新 Xbox One 游戏机的所有者只能在易贝找到一个适配器，那里的价格自然会飙升。

[![](img/5c5f23fa2fca173c69dfb1ea4dd06074.png)](https://hackaday.com/wp-content/uploads/2018/02/kinect_detail.jpg) 最近【Eagle115】决定打开他的 Kinect，看看他能否[找到一种方法把它连接到他的新 Xbox One](https://imgur.com/a/e10dN) 。Kinect 上的端口是 USB 3.0 B 母接口，但需要 12V 才能工作。官方的 Kinect 适配器采用了一个[独立交流适配器和一个通过 USB 为 Kinect 提供 12V 电源的“tap”](https://support.xbox.com/en-US/xbox-one/accessories/kinect-adapter)的形式，所以他认为他可以打开设备，直接向 PCB 上的焊盘供电。

[Eagle115]买了一个 12V 墙壁适配器和一根 USB 3.0 B 线，开始工作。一旦 Kinect 被打开，他发现他需要在第 10 号针脚上供电(这在 PCB 上有很好的标签)。只有足够的空间让交流适配器的电缆穿过 USB 电缆连接的同一个孔。

由于 Kinect 从交流适配器获得 12V 电压，Xbox 可以毫无问题地检测到它，就像您使用的是官方适配器一样。至少目前，他们还没有取消 Xbox 操作系统对 Kinect 的支持。

Kinect 一直非常受黑客的欢迎(它甚至在 Hackaday 上有自己的类别)，所以看到微软放弃这款产品绝对令人难过。毫无疑问,[社区将会继续用它完成令人敬畏的黑客任务。但是看起来我们越来越不可能得到下一代 Kinect 了。](https://hackaday.com/2015/08/22/augmented-reality-sandbox-using-a-kinect/)

[通过 [/r/DIY](https://www.reddit.com/r/DIY/comments/7xz61n/this_may_have_a_limited_audience_here_but_i/)