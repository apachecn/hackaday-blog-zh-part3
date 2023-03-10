# 反向模仿 NES:任天堂！

> 原文：<https://hackaday.com/2018/05/31/reverse-emulating-nes-nintendception/>

伙计们，这是一个一流的黑客。[Tom7]用一个非常可爱的技巧，在一台普通的老任天堂游戏机上实现了全动态视频和运行超级任天堂游戏。他展示了他是如何在任天堂上做到的——任天堂动力(point)！“是什么”和“怎么做”将在下面的两个视频中解释。

在第一部的[中，他展示了这一切，并给你一个概述。就这么简单:任天堂系统在 ROM 卡盒中存储 8×8 像素的游戏图形块，运行的程序将这些图形块取出并显示出来。如果您不局限于将这些块存储在 ROM 中，比方说，如果您用 Raspberry Pi 替换了墨盒，您可以发送自己的图形进行显示。](https://www.youtube.com/watch?v=ar9WRwCiSr0)

他通过这样做演示了一个熟悉的红头发英国灵魂乐歌手的视频——每次通过显示循环，树莓 Pi 都会重新计算“恒定”图像块以制作视频。然后他加大赌注，在 Pi 上模拟 SNES，在模拟中玩一个永远不可能在 NES 上玩的游戏，并将图形逐块发送回任天堂。太棒了。

第二个视频详细讲述了他是如何做到这一点的。我们尤其喜欢他的史诗般的方法:至少花一天时间试图证明这是不可能的，当你排除了所有严重的阻碍因素后，你就知道这很有可能行得通。然后，开始工作。我们还了解到，有些电容器看起来与 80 年代中期日本使用的电阻器相同。

这些都是长视频，第一个视频以一些疯狂的猜测结束，关于类似的人类大脑增强如何采取类似的方法，用动态计算的数据取代我们的“记忆”。(等等，什么？！？不过，这是个很酷的主意。)还有另一个主题贯穿了第一个关于幽默的视频，但坦率地说，我们没有理解这个笑话。或者我们只是不知道什么是好笑的。评论？

这些都不重要。一个 SNES 游戏是在一个 NES 上进行的，通过实时从一个“rom”盒中推出修改过的图形。这太棒了！

如果你想要更多的任天堂游戏，看看这个 NES 的 ROM，它也是一个包含自己源代码的压缩文件。如果您编译源代码，您将获得 zip 文件，如果您解压缩该文件，您将获得要编译的源代码。对吗？

 [https://www.youtube.com/embed/ar9WRwCiSr0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ar9WRwCiSr0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/hTlNVUmBA28?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hTlNVUmBA28?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢每一个把这个发到举报热线的人！[darks prte]，[Erik S]，[Reversnes]，[Tim Trzepacz]，[KAN]，[Jorhlok]和[Qes]。(我忘记谁了吗？！？)