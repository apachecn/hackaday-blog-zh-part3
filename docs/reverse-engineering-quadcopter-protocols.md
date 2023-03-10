# 逆向工程四轴飞行器协议

> 原文：<https://hackaday.com/2016/06/28/reverse-engineering-quadcopter-protocols/>

需要是发明之母，但来自中国的廉价垃圾是逆向工程之母。[迈克尔]在他当地的商店里发现了一个非常非常便宜的玩具四轴飞行器，并向自己发出了挑战。他会逆向工程这个四轴飞行器的无线电协议。他的四篇文章系列包括为无线电找到正确的频率，找出协议，并为这个便宜的玩具制作自己的遥控器。

[迈克尔]在阅读了一篇黑客帖子后，已经熟悉了这些廉价玩具的功能，这本 75 页、4 种语言的手册为他澄清了一些事情。“Quadro-Copter”工作在 2.4GHz，但没有给出任何进一步的信息。[迈克尔]不知道玩具在哪个频道接收，什么数据速率，或者传输的报头是什么。SDR 将是解决这一问题的好工具，但多亏了 Travis Goodspeed，[有一个非常巧妙的技巧](http://travisgoodspeed.blogspot.fr/2011/02/promiscuity-is-nrf24l01s-duty.html)，将 2.4GHz nRF24L01+无线电置于混杂模式，允许【迈克尔】读取发射机和四轴飞行器之间的传输。这段代码可以在[【迈克尔】的 github](https://github.com/m-melchior/QC-360-A1/tree/master/src/Arduino/myRF24PromiscuousReceiver) 上找到。

在电磁干草堆里找到了一根针，迈克尔可以监听四轴飞行器的指令。[下一步是解释 1 和 0](https://mmelchior.wordpress.com/2016/06/15/qc-360-a1-p2/)，在一个小型分线板的帮助下，并直接焊接到发射器的 SPI 总线上，【Michael】能够做到这一点。通过阅读 nRF24 文档，他能够找出配对协议，并读取命令四轴飞行器的字节流。

[迈克尔]剩下的是一系列八个字节，以连续流的形式从发射器发送到玩具。这些字节包含油门，偏航，俯仰，滚动和一个“翻转”设置，以及三个字节的“计数器”，似乎没有做任何事情。有了这些信息，[Michael]拿了一台 Arduino Nano、一台 nRF04L01+收发器和一个 Wii nunchuck 来建造他自己的发射器。如果你正在寻找一个“如何逆向工程”的指南，通常没有比这更好的了。

你可以看看下面[迈克尔]驾驶他的遥控四轴飞行器的视频。

 [https://www.youtube.com/embed/p83ooaU7QZw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/p83ooaU7QZw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

