# 终于有人用 555 做到了

> 原文：<https://hackaday.com/2017/08/22/someone-finally-did-it-with-a-555/>

[Jarunzel]需要一个能在预设的时间间隔自动点击鼠标左键的设备。对于普通的黑客读者来说，这是一个简单的挑战。你可以用一台使用 VUSB 库的 ATtiny85，几个电阻和二极管，以及一段模拟 USB 设备的代码来实现，该设备每隔几秒钟就不断地通过 USB 发送鼠标点击。你也可以用一个 Raspberry Pi Zero，使用 USB 小工具协议来实现。现在，这个点击鼠标的小工具将连接到互联网上。)，可以用 Node 或现在孩子们用的任何东西来编程，并且会有一些主要的博客信誉。如果你喜欢冒险，这个鼠标点击小工具可以用 STM32、Cypress PSoC 或你的黑客魔术包中的任何微控制器来构建。

另外，你也可以用 555 定时器来做这件事。

原因是[Jarunzel]不能使用任何花哨的黑客工具，因为系统不接受两个鼠标设备。没关系，因为 Maplin [有一个带有 555 定时器和继电器的整洁套件](https://www.maplin.co.uk/p/555-astable-switch-kit-n33fl)。继电器跨接在鼠标中的微动开关上，正确设置值会使鼠标每秒钟点击一次，点击持续时间约为 100 毫秒。够好了。

随着工具包的建立，连接到鼠标，一个测试设备的小应用程序的建立，一个漂亮的项目盒的构建，[Jarunzel]拥有了他所需要的一切。甚至还有一个这个鼠标点击器的视频。你可以看看下面的精彩片段。

 [https://www.youtube.com/embed/H6IccgLMmr0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/H6IccgLMmr0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

