# 激光指针钟使得计时成为一件旷日持久的事情

> 原文：<https://hackaday.com/2016/11/04/laser-pointer-clock-makes-timekeeping-a-drawn-out-affair/>

设计一个独特的时钟来展示你的技术技能会是一次有益的经历，并为你的家带来令人钦佩的展品。[Andres Robam]看到了一个机会，可以制造一个激光指针时钟，将当前时间画在一个夜光标签上。

一对步进电机倾斜和平移激光器支架——在 SolidWorks 中设计并 3D 打印。电机轴有一个问题，它有些松弛，足以影响激光的精度。[Andres]通过使用笔的弹簧在系统中产生足够的张力来纠正它，巧妙地解决了这个问题。NODEmcu v2 是时钟的大脑——选择它是因为它内置的 WiFi 功能和与 Arduino IDE 的兼容性——一个 5mW 的激光将时间写在贴纸上。

 [https://www.youtube.com/embed/gf07ROyVDsA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/gf07ROyVDsA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



如果你想为自己建造一个这样的东西，这个时间是从一个网络服务器上获取的，这个服务器被编码并发布到 GitHub 上。或者，你可以选择一个浮动的 T2 时钟，而不是激光时钟。