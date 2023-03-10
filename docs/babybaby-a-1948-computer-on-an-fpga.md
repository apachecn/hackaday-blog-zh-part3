# baby baby:FPGA 上的 1948 年计算机

> 原文：<https://hackaday.com/2016/01/06/babybaby-a-1948-computer-on-an-fpga/>

曼彻斯特婴儿今天看起来很简单。一台有 32 个字存储空间的 32 位机器。不过，它并不意味着是一台电脑，而是新的威廉姆斯电子管存储设备的测试平台。然而，在 1948 年，它以每秒 1100 条指令的速度执行存储的程序。这种机器的成功导致了曼彻斯特大学的一系列计算机，并最终导致了第一台商用计算机，即 Ferranti Mark I。

[戴夫]很幸运地自愿在马彻斯特科学工业博物馆展示婴儿复制品。他想要自己的宝宝，所以他使用 Xilinx FPGA 板制造了一个名为 BabyBaby 的复制宝宝。尽管它的运行速度与原机相同，但幸运的是，它比真机小得多。

尽管 VGA 显示器取代了 CRT 屏幕，但[Dave]的结构仍然忠实于原始的外观和感觉。你可以在下面的视频中看到 BabyBaby 的演示。实现是用 VHDL 语言进行的，考虑到 VGA 接口，可能比原来的机器更复杂。

以今天的标准来看，宝宝的指令集非常简单。唯一可用的数学运算是减法和否定。由于一个简单的加法需要 32 条指令中的 4 条，可以想象你不可能做太复杂的事情。尽管如此，对于 550 支功率约为 3.5 千瓦的电子管来说，这在 1948 年仍是一个奇迹。

奇怪的是，这不是我们看到的第一个婴儿重建。还有一个[缩小版的 8 位版本](http://hackaday.com/2015/06/23/really-really-retro-computer-on-an-fpga/)。我们甚至看到了婴儿的后代——马克一世—[演奏音乐，这可能是已知最古老的电脑合成音乐](http://hackaday.com/2008/06/17/worlds-oldest-computer-music-unveiled/)。

 [https://www.youtube.com/embed/OGcAmrFoRrY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/OGcAmrFoRrY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

