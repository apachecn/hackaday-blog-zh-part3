# Rubik 的解决方案使用 FAC 机器制造系统

> 原文：<https://hackaday.com/2015/09/15/rubiks-solver-uses-fac-machine-building-system/>

我们喜欢好的魔方解算器，这个机器人的机械工程既优雅又实用。

这是我们第一次听说[FAC 系统](http://www.facsystem.se/default_eng.asp)，这是一套标准零件，可用于制造任何数量的机械系统。[威尔伯特·斯文克尔斯]必须是系统的大师；尽管内置了多个自由度，但机器的布局看起来简单而不拥挤。这些包括一个用于放入和取出立方体的插入平台，一个用于三个颜色传感器的门架，以及两个用于实际求解的轴(总共三个夹具)。如果你以前用过 FAC，我们想听听你对它的看法。

[Maxim Tsoy]处理运行在 [Rapsberry Pi 计算模块](http://hackaday.com/2014/04/07/the-raspberry-pi-compute-module/)上的软件。你会想看下面的演示视频。首先，将随机化的立方体放在插入平台上，当立方体被夹子夹住后，插入平台缩回。这些工作与颜色传感器机架一起扫描立方体的每一面。在短暂停顿以计算解决方案后，夹持器开始工作。

有可能建立一个只有两个旋转夹具的解算器。这里有一个非常快速的方法。

 [https://www.youtube.com/embed/vpAKfSYueMI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/vpAKfSYueMI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[via [reddit](https://www.reddit.com/r/raspberry_pi/comments/3l0x7o/rubix_cube_solver_that_uses_a_pi_compute_module/)