# 快速原型制作 RF 滤波器

> 原文：<https://hackaday.com/2017/07/25/rapidly-prototyping-rf-filters/>

RF 滤波器实际上只是一些精心放置的电感和电容。是的，可以用通孔元件制作 1 GHz 滤波器，但在这些频率下，器件上的引脚会变成电感，完全破坏设计的预期效果。

解决方案是微带天线，或者是 PCB 上精心布置的走线和焊盘。任何人都可以用 Eagle 或 KiCad 建造其中的一个，但这意味着要等待董事会的订单来验证你的设计。[VK2SEB]有一个更好的 PCB 滤波器原型的想法:[在空白 FR4 片上使用铜带](https://www.youtube.com/watch?v=drwGvATLNaw)。

第一个也是最简单的滤波器是一个简单的带阻滤波器。这实际上只是一片玻璃纤维，一面层压了铜。两个射频连接器焊接在边缘，中间有一条铜带。在这个铜带中间的某个地方，[VK2SEB]将另一条铜带放在一个“T”形配置中。这是你能做的最简单的带阻滤波器，这种结构的美妙之处在于它可以用刀片来调谐。

当然，如果你能设计出滤波器，它只能用铜带制作，为此[SEB]转向了软件。[Qucs 项目](http://qucs.sourceforge.net/)是一个设计和仿真这些微带滤波器的软件工具，在输入正确的参数后，【SEB】得到了一个滤波器应该是什么样子的漂亮图。一些胶带，刀片，焊接和[SEB]有一个连接到频谱分析仪的工作过滤器。成功了吗？在有限的程度上；PCB 材料可能不正确，板房比刀片更精确，但[SEB]确实成功地用玻璃纤维和铜带制造了一个 10 GHz 的滤波器。

你可以看看下面这个实验的视频。

 [https://www.youtube.com/embed/drwGvATLNaw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/drwGvATLNaw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

