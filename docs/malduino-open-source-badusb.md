# MalDuino —开源 BadUSB

> 原文：<https://hackaday.com/2017/01/24/malduino-open-source-badusb/>

MalDuino 是一个 Arduino 驱动的 USB 设备，它模拟键盘并具有击键注入功能。它仍处于众筹阶段，但已经得到了充分的支持，所以我们预计很快就会全面生产。本质上，它实现了 BadUSB 攻击，就像广为人知的一样，出现在*的机器人先生*，USB 橡皮鸭上。

这就像是我们之前报道的高级版本的[隐藏掉恶意文件](http://hackaday.com/2015/01/27/using-hid-tricks-to-drop-malicious-files/)的诡计。一旦插上电源，MalDuino 就像一个键盘，以极快的速度执行之前配置的按键序列。这主要是 IT 安全专业人员用来侵入本地计算机的，只需插入可疑的 USB“笔”即可。

MalDuino 的制造商[Seytonic]表示，它的目标是成为一种更便宜、完全开源的替代产品，其巨大优势是可以直接从 Arduino IDE 中编程。它基于 ATmega32u4，像 Arduino Leonardo 一样，并将有两种口味，Lite 和 Elite。Lite 非常小，几乎可以放入任何通用 USB 盒中。有一个开关用于启用/禁用器件编程。

精英版是令人兴奋的地方。除了将用于存储脚本的 MicroSD 插槽之外，还有一组板载 dip 开关，可用于选择要运行的脚本。由于整个平台是开源的，并且基于 Arduino，所以 MicroSD 插槽和 dip 开关完全是模块化的，没有什么是硬编码的，你可以使用它们做任何你想做的事情。BadUSB 攻击的最熟练的使用者已经展示了类似于[建立一个假的有线网络连接](http://hackaday.com/2014/10/05/badusb-means-were-all-screwed/)的壮举，它允许所有的网络流量被虹吸到外部服务器。虽然不是 MalDuino 的默认固件，但使用这里使用的微控制器应该是可能的。

对于大多数用户来说，典型的功能攻击可能包括改变 dip 开关的用途，以修改特定脚本的设置。除了在 MicroSD 卡上存储脚本，你还可以在上面存储单词列表，用于破解密码。看看人们会想出什么和他们创建的脚本会很有趣，因为有很多空间可以修补和增强它。这就是开源的伟大之处。

您可以在视频中观看运行中的原型:

 [https://www.youtube.com/embed/nNDWdmJI6bw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/nNDWdmJI6bw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

