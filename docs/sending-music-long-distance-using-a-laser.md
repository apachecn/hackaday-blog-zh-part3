# 用激光远距离传送音乐

> 原文：<https://hackaday.com/2016/09/25/sending-music-long-distance-using-a-laser/>

这不是我们第一次看到 DIY 者通过激光束发送音乐，但兄弟[Armand]和[Victor]肯定在争夺从他们的建筑发送音乐的最长距离，452 米/1480 英尺，越过几栋房子的屋顶，穿过树顶，进入朋友的公寓。接收到的声音质量也相当惊人。

如果你以前从未遇到过这种情况，激光的光被直接来自音频源的信号调制，使其成为模拟传输。激光器是从易贝购买的 250mW 二极管激光器。它通过一个由 12V 电池供电的 5 伏 7805 电压调节器供电。来自声源的信号通过升压变压器进入电路，将其隔离，这样就不会有来自声源的 DC 进入。变压器的激光器一侧给晶体管的基极供电。他们包括一个开关，这样来自调节器的电流可以通过由声源控制的晶体管的集电极和发射极，进行强调制，或者电流可以直接进入激光器，而调制只通过晶体管的基极和发射极提供。电路原理图在他们视频的最后给出，休息后你可以看到。

他们在朋友的公寓里使用太阳能电池接收光束，然后将光束输入一个相当大的放大器和扬声器。从视频中，你可以听到令人惊讶的高品质的声音。所以去看看吧。它还包括一点班尼·希尔式的幽默。

 [https://www.youtube.com/embed/DtCwJU6YMaA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/DtCwJU6YMaA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们以前什么时候见过激光通信？为什么你的真的演示了一个短程传输[使用一元店宠物玩具激光](http://hackaday.com/2015/07/02/solar-cell-laser-communication-system/)发送到太阳能电池和自制放大器。如果你想深入了解，[千兆位激光以太网](http://hackaday.com/2016/03/10/gigabit-ethernet-through-the-air/)正是你想要的。