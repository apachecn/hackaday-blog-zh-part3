# 进入太空隧道

> 原文：<https://hackaday.com/2017/02/26/enter-the-space-tunnel/>

有什么比 1 串 LED 灯更好？96.就这么多。96 的每个串有 60 个 ws2812b LEDs，总共有 5760 个可单独寻址的 RGB LEDs。这还不是[jaymeekae]的太空隧道装置最酷的部分，[最酷的部分是它们是互动的](http://imgur.com/gallery/FEhMI)。

从一些聚氯乙烯管道开始，深色布被用作背景，LED 灯条附在上面。几个电源用于提供必要的电压，每个条带由通过 USB 连接到 Windows PC 的 [FadeCandy](https://www.adafruit.com/product/1689) 芯片控制。最初，使用计算机电源，但它们无法提供必要的电流。[jaymeekae]在第一次安装时使用了它们，但在以后的安装中改用了更好的电源。

一旦灯亮起并通电，[jaymeekae]就开始在界面上工作来控制它们。从一个用过的柜子开始，[jaymeekae]切下一部分作为触摸屏，并在下半部分安装了控制计算机。Processing 用于与 FadeCandy 控制器交互，HTML 用于用户界面。每种模式都运行不同的处理程序来实现不同的效果，包括音频可视化、空间隧道模式(因此得名)和一个很酷的绘图应用程序，用户可以在触摸屏上绘图，并在头顶的灯光下看到结果。

经过几次迭代，太空隧道已经得到了发展，有了更好的电源和更好的接口。这是一个很棒的艺术装置，[jaymeekae]带着它去参加艺术节，包括西班牙和英国的艺术节。Hack-a-Day 还有其他一些 LED 灯串项目，包括用乒乓球做的[这个](https://hackaday.com/2013/12/20/an-even-larger-array-of-many-leds-and-no-ping-pong-balls/)和[这个](https://hackaday.com/2016/06/03/1575-bottle-of-beer-on-the-led-wall/)需要先喝很多啤酒。

[通过 Reddit]

 [https://www.youtube.com/embed/oOJRWrsfEa4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/oOJRWrsfEa4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/ydAGQ7scHfI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ydAGQ7scHfI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

