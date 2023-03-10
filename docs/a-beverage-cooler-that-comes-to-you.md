# 来到你身边的饮料冷却器！

> 原文：<https://hackaday.com/2017/07/02/a-beverage-cooler-that-comes-to-you/>

想走很长一段路，但又不想带饮料？别害怕，这个[“跟我来”的酷酷机器人](https://www.hackster.io/hackerhouse/make-an-autonomous-follow-me-cooler-7ca8bc)就在这里！

这只是一个移动平台，顶部有一个冷却器，机器人通过蓝牙连接到智能手机，使用 GPS 跟踪它。制作这个平台需要一点木工技巧，一个带有 3D 打印轮毂适配器的铝轮毂将电机连接到一对 6 英寸的橡胶轮上，后面安装了一个旋转脚轮。平台底部的一个口袋里装着电子设备。

Arduino Uno 通过 L298n 电机驱动器控制两个安装在 3D 打印支架上的 12V DC、有刷和齿轮电机，而 Parallax PAM-7Q GPS 模块与 HMC 5883L 指南针一起帮助机器人保持方位。电池阿朵分别为电机和电子设备供电，以防止任何故障。

 [https://www.youtube.com/embed/vGDMpLMkWFg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/vGDMpLMkWFg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



使用 Blynk 在 Android 智能手机上控制平台。易于使用，能够设置基本命令，通过所需的连接类型发送给机器人，这使它成为这个有用的小“机器人”的理想选择。

没有任何更复杂的事情发生——比如避障或复杂的寻路——所以你需要在你和冷却器之间划出一条清晰的线。尽管如此，饮料存储是一个很好的功能，可以添加到你的跟屁虫机器人伴侣中。它似乎工作得很好。