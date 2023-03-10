# 这只老老鼠记录灯丝的使用情况

> 原文：<https://hackaday.com/2016/12/08/this-old-mouse-keeps-track-of-filament-usage/>

记录 3D 打印机灯丝的使用情况既让人大开眼界，又让人沮丧。确切地知道一个项目需要多少材料可以帮助你做出制造还是购买的决定，但当你看到你在那张失败的印刷品上花了多少钱时，这也可能会令人心痛。库存细丝计数器并不总是非常准确，但是你可以从一个旧鼠标中推出你自己的[细丝计数器。](https://hackaday.io/project/18804-coversion-of-ps2-mouse-to-filament-counter)

[孙斌]的构建是基于一个旧的球型 PS/2 鼠标，带有漂亮的光学编码器的那种。如今，这种年份的老鼠越来越难得到了，但你可能已经在垃圾箱里找到了一只，或者可以从旧货店淘到一只。剥去内脏，用一个 3D 打印的支架固定住，用来感应球旋转的辊子在细丝进入挤压机的途中对其施加压力。Arduino 跟踪脉冲并累计使用的灯丝数量；当灯丝缩回时，计数器很方便地从总数中减去。

简单、有用、便宜——这就是黑客的定义。即使你没有 3D 打印机，从老老鼠身上收集编码器也是一个不错的技巧，以备不时之需。或者你可能更喜欢为你的下一个项目建立你自己的编码器。

 [https://www.youtube.com/embed/kwaZ24wySXI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/kwaZ24wySXI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

