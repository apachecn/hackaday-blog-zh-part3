# 用几根线打败芯片和引脚

> 原文：<https://hackaday.com/2015/11/25/defeating-chip-and-pin-with-bits-of-wire/>

美国人被世界其他地方嘲笑的原因之一是他们的信用卡上还没有芯片和密码；美国信用卡公司在将这项技术引入全国数百万台 POS 终端方面进展缓慢。进行转换并不容易，因为在转换完成之前，机器必须接受磁条以及芯片和 PIN。

通过强制降级到磁条，该设备可以无线禁用芯片和 PIN 码。[Samy Kamkar]创建了 MagSpoof 来探索他的美国运通卡磁条上的二进制图案，并在此过程中还创建了一个与驾照、酒店房间钥匙和停车计时器配合使用的设备。

MagSpoof 的电子设备极其简单。当然，一个小的微控制器对于这个构建是必要的，对于 MagSpoof，[Samy]使用 ATtiny85 作为“更大”的版本(仍然小于一平方英寸)。一个更小的，信用卡大小的版本使用的是 ATtiny10。原理图的其余部分只是一个 H 桥和一个电磁线线圈——对于任何有烙铁的人来说，在某个 perfboard 上组装起来都很容易。
通过对 H 桥施加脉冲并给线圈通电，MagSpoof 模仿了信用卡的刷卡行为——这只是磁场以一种非常特殊的模式反转方向。由于任何信用卡上的磁性图案都可以很容易地被读取，而且[Samy]证明了用一些铁锈和肉眼也可以做到这一点，所以通过构建一些电子设备来克隆一张卡是一件很简单的事情。

[萨米]没有就此打住。通过关闭表明卡*上有*芯片的位，他的设备可以绕过芯片和 PIN 保护。如果你非常小心地使用磁针，你可以禁用任何信用卡上的芯片和密码保护。[Samy]的设备不需要那么灵活——他只需在 MagSpoof 的固件中翻转一下即可。这都是出色的工作，虽然芯片和 PIN 码失败的代码不包括在回购协议中的，但显示如何做到这一点的文件确实存在。

[Samy]的实现很工整，但是站在巨人的肩膀上。特别是，我们之前已经讨论过类似的设备(例如，这里的[和这里的](http://hackaday.com/2010/11/02/magnetic-card-stripe-spoofer/)[和](http://hackaday.com/2008/08/04/magnetic-stripe-card-spoofer/))，除了芯片和引脚降级攻击之外，你在这次黑客攻击中需要的一切都在【零计数】1992 年的经典作品[通量逆转的一天](http://phrack.org/issues/37/6.html)中讨论过。

感谢[托鲁]送来这封信。下面是[Samy]的视频。

 [https://www.youtube.com/embed/UHSFf0Lz1qc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/UHSFf0Lz1qc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

