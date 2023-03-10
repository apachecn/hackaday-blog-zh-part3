# 黑掉一台 30 年前的俄罗斯 VFD

> 原文：<https://hackaday.com/2018/03/03/hacking-a-30-year-old-russian-vfd/>

Reddit 用户[InThePartsBin]在易贝的一块旧 PCB 上发现了一些 VFD(真空荧光显示器)。俄罗斯的电路板可以追溯到 1987 年，有一堆通孔电阻器、晶体管和一些神秘的集成电路，塑料包裹着腿，管子的顶部由橡胶垫圈固定(尖端本身穿过垂直于主板安装的电路板上的孔。)他是我们喜欢的那种好奇的人，看到这些板子不太贵，他买了一些来玩，看看他是否能让它们起死回生。

在点亮了 VFD 并弄清楚了背面的电路之后，[InThePartsBin]决定用它来制作一个时钟是最好的。人们认为专门的 VFD 驱动芯片是最简单的工作方式，因此订购了 MAX6934。为了给时钟一些大脑，招募了一个 ATmega328，为了保持时间，[InThePartsBin]有一些以前项目遗留下来的 DS3231 实时时钟模块，所以他们也被招募了。子板被设计成位于老式板的背面，并容纳 328 和 VFD 驱动芯片。

一旦[InThePartsBin]焊接到组件上，就该启动它并向驱动器发送 1 来打开所有电子管上的所有部分。成功！[InThePartsBin]剩下唯一要做的就是写时钟的代码，但是现在所有的段和管都是可控的，所以硬件部分已经完成了。现场还有其他 VFD 时钟项目:看看这个[一个](https://hackaday.com/2016/01/25/vfd-430-clock-nyc-style/)，或者这个[一个](https://hackaday.com/2016/08/24/vfd-clock/)，晒晒美丽的钢蓝色光芒。

Via [Reddit](https://www.reddit.com/r/electronics/comments/7tx8wv/projects_log_hacking_a_30_year_old_russian_vfd) 。