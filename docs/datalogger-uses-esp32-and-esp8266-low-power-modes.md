# 数据记录器使用 ESP32 和 ESP8266 低功耗模式

> 原文：<https://hackaday.com/2017/09/24/datalogger-uses-esp32-and-esp8266-low-power-modes/>

[G6EJD]想要设计一款低功耗数据记录器，并决定对比一下 [ESP32](https://www.youtube.com/watch?v=DDpuBJYFJ7Y&t=3s) 和 [ESP8266](https://www.youtube.com/watch?v=LZrF1GzMfN8&t=4s) 的功耗。你可以在下面看到视频结果。

当然，每当有人做能力测试时，你必须想知道是否有任何技巧或变化会产生很大的不同。然而，相对数据是有趣的(尽管你可以假设甚至那些结果也会误导人的情况)。您应该观看视频，但底线是 3000 毫安时电池可为 ESP8266 提供 315 天的运行时间，为 ESP32 提供 213 天的运行时间。

事实上，硬件和软件只是在中央处理器上有所不同，这意味着结果应该非常相似。[G6EJD]说明整个电路的电流消耗。天数是用数学计算出来的，所以不能反映实际使用情况。还要看你单位时间取多少样。目标是让电池运行一年，如果你愿意降低采样率，这是可能的。

虽然我们一般喜欢 ESP32，但[G6EJD]指出，如果电池寿命对你来说很重要，你可能想坚持使用 ESP8266，或者寻找其他产品。自然地，如果你试图最大限度地延长电池寿命，你将不得不[大量睡眠](https://hackaday.com/2016/11/11/esp8266-lullaby/)。

 [https://www.youtube.com/embed/DDpuBJYFJ7Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/DDpuBJYFJ7Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/LZrF1GzMfN8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LZrF1GzMfN8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

