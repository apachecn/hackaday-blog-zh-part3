# Extech 电源:如果没坏，那就修好它

> 原文：<https://hackaday.com/2016/12/15/extech-power-supply-if-it-aint-broke-fix-it-anyway/>

[狼]得到了一个不太好用的 Extech 电源。它被用于电池制造，已经被严重腐蚀。他修好了它[,但发现电源有问题，而这不是故障](http://www.wolftronix.com/extech/index.html)。根据设计，当关闭输出时，电压表的读数为零。这意味着你不能在不打开输出的情况下将电压调整到一个已知值。当然，你应该在调整之前把事情分开，但是你只能希望你会记得。

起初，他试图使用现有的输出控制开关，但那真的会切断电源。相反，他转向通常用于伺服控制的小型微控制器板。他在前面板上加了几个好看的按钮。外壳中有足够的空间来安装控制板和四个继电器。你可以在下面的视频中看到最终的结果。

剩下的你可以猜。该微处理器能够读取控制，设置电源，并关闭输出，而不影响计量。顺便说一下，这需要对输出终端进行一些大的机械手术。此外，微处理器通过模数转换器监控电压输出，并在掉电时存储状态。这样，它可以在下一次电源事件时恢复正常。

[Wolf]制作了八个视频，涵盖了整个过程的每一步。你可以在下面的视频中找到结果，但一定要看那些导致它的视频。

Extech supply 看起来不错，但我们注意到，由于一些有趣且便宜的模块，构建自己的 Extech 变得越来越容易。如果你愿意，你也可以[一件件](http://hackaday.com/2016/02/06/build-yourself-an-awesome-modular-power-supply/)地建造一个。

 [https://www.youtube.com/embed/rD9JmLsDykM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rD9JmLsDykM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

