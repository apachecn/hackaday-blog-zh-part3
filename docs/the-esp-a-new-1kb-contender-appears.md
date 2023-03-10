# ESP:一个 1kB 的新竞争者出现了

> 原文：<https://hackaday.com/2016/11/30/the-esp-a-new-1kb-contender-appears/>

ESP8266 正式进入黑客日 [1kB 挑战](https://hackaday.io/contest/18215-the-1kb-challenge)。在 1kB 的编译代码中做一些有意义的事情是很棘手的；现代的 SDK，比如经常用于 ESP8266 的 SDK，甚至可以将最简单的程序编译成接近那个大小。如果你想在 1kB 挑战赛中使用这个硬件，我有一个解决方案给你！

ESP8266 现在有一个准系统构建环境，专注于最小化代码大小，只有 131 个字节来启动和闪烁 LED。它还“支持”一些新的、疯狂的时钟频率(如 346 MHz)和疯狂的开发周期速度。WiFi 停留在“飞行模式”，但值得你花时间考虑下一个非 WiFi 项目的 ESP。

太多时候，我们遵循“只工作”的设计模式，而不是寻找最佳的，因为我们害怕浪费时间。保持代码紧凑和短小的好处经常被忽视。当代码很小且环境最小时，RAM 和闪存变得更容易获得，编译后的二进制文件变小，编译和闪存所浪费的时间可以减少一个数量级！当我们成为一名优秀的工程师时，我们很少看到增加了多少价值:只有当设计中没有什么需要删除的时候，我们才会去做。Nosdk8266 将让你看到一分钟内测试几次代码变化是什么感觉。

就在一个月前，在为一个 [USB 引导程序](https://github.com/cnlohr/espusb/tree/master/bootloader)准备 ESP8266 时，我不得不为它制作一个精简的环境。它不是基于[官方非操作系统 SDK](http://bbs.espressif.com/viewforum.php?f=46) 或 [RTOS sdk](https://github.com/espressif/ESP8266_RTOS_SDK) ，而是一个可以启动和闪烁 LED 的环境。不只是闪烁 LED，而是以一些完全意想不到的方式调整时钟，甚至运行 I2S 总线(用于[以太网](https://hackaday.com/2016/04/01/ethernet-controller-discovered-in-the-esp8266/)和[彩色 NTSC 广播视频](http://hackaday.com/2016/03/01/color-tv-broadcasts-are-esp8266s-newest-trick/))。如果你不在 1kB 挑战的提交阶段，你甚至可以使用 printf 的 mask ROM！现在你可以调整你的代码——在 2 秒钟之内——看看新代码做了什么！

 [https://www.youtube.com/embed/AWT2w7v9szs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/AWT2w7v9szs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



即使在 PICO 模式下，器件仍然需要使用屏蔽 ROM 来加载，但幸运的是，[1kB 挑战](https://hackaday.io/contest/18215-the-1kb-challenge)为不可避免的引导加载程序增加了一个例外。不再受 WiFi 的束缚，我迫不及待地想看看你会用 ESP8266 做什么。请注意，当超频到 346 MHz (332.5%)时，处理器可能无法可靠地工作，并且您肯定会使您可能拥有的任何保修失效。听起来很有趣，对吧？

编辑注释:这是查尔斯·洛尔(Charles Lohr)的一篇客座文章。尽管他写过一些其他的客座文章，但他并不是 Hackaday 的定期撰稿人，因此，这篇文章并没有取消他参加 1kB 挑战赛的资格。我们觉得发表这篇文章更公平，它分享了他用来使代码更小的工具，而不是因为害怕失去资格而把它们留给自己。虽然您已经注意到了，但我们想提一下 Charles 在 4 月 1 日发表的一篇文章——我们仍然认为有很多人没有意识到[这不是一个恶作剧](https://hackaday.com/2016/04/01/ethernet-controller-discovered-in-the-esp8266/)。