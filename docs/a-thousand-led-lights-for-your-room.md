# 为您的房间提供一千盏 LED 灯

> 原文：<https://hackaday.com/2015/10/03/a-thousand-led-lights-for-your-room/>

当然，你可以像正常人一样拥有一个普通的灯具…或者你可以使用近 1000 个 RGB LEDs 来照亮你的房间！

这就是[德米特里]在试图找出点燃他的垫子的最佳方式后决定要做的。你看，他的房间是 4 乘 4 米，而 WS2812 RGB LED 灯条恰好有 4 米长……巧合？我们认为不是。

使用 16 米长的 LED 灯条的问题是为它们供电…你看，在 16 米处，你看到的是大约 5V @ 57.6 a——我们猜测你手边可能没有 5V 60A 的电源。更不用说，如果你串联运行它们，系统的电阻会降低你的效率，最后的 led 可能甚至不会工作…所以[Dmitry]不得不打破这个系统。他有两个电源从每一对的中间向条带供电，这样，他就不必担心由于条带的长度而产生的任何电压降。

控制它们是下一个有趣的部分。使用一个 ATMega 和一个 [Nordic FOB](https://www.sparkfun.com/products/retired/8602) (停产但有用的射频遥控器)，他能够控制灯光做他想做的任何事情——他也在自己的网站上分享了资源。

 [https://www.youtube.com/embed/pT73PRrmi-c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/pT73PRrmi-c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



对于一个更奇特的 LED 房间设置，[来看看这个雕刻的 LED 照明房间](http://hackaday.com/2013/12/24/fubarino-contest-a-sculpted-room-with-leds/)，它看起来更像一个冰窟！