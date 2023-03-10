# 零侵入无线照明开关

> 原文：<https://hackaday.com/2017/03/14/zero-intrusion-wireless-light-switch/>

如果你的电灯开关离你的桌子太远，而你是在一个租来的房子里，所以你不能为它安装额外的电线来安装电子控制，你会怎么做？起来用手开还是关？当然不是！

如果你是[Guyfromhe]，[你用一个连接到螺旋灯开关面板](http://guyfromhe.blogspot.co.uk/2017/03/wireless-lightswitch-mark-ii.html)的伺服系统解决这个问题，你用一对 Arduino/nRF24L01 组合控制它。这是一个非常简单的安排，无线链接只是取代了串行电缆，指示灯开关上的 Arduino 操作伺服系统，进而移动开关。整个事情是通过他的家庭自动化系统触发的，而家庭自动化系统又会对他桌子上的亚马逊 Dash 按钮做出反应。是的，很复杂。但是开灯是自动的，并没有侵犯他房东的领地，这才是最重要的。

更严重的是，他在他的文章中放了一些 Arduino 代码，以及我们放在休息时间下面的 YouTube 视频。

 [https://www.youtube.com/embed/IDM3BPzUKHo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/IDM3BPzUKHo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



这绝不是我们看到的第一个这样的开关，毕竟几个月前我们展示了[一个更好的 3D 打印伺服灯开关](http://hackaday.com/2017/01/17/servo-controlled-iot-light-switches/)，以及 2015 年一个带有试验板 Arduino 的[。虽然我们在这里，但也很高兴看到一些为欧洲交换机设计的产品。](http://hackaday.com/2015/11/06/the-robot-light-switch/)