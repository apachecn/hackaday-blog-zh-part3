# BrickerBot 会永久移除您的物联网设备

> 原文：<https://hackaday.com/2017/04/08/brickerbot-takes-down-your-iot-devices-permanently/>

现在有一种新的 virii，专门针对物联网(IoT)设备。BrickerBot 及其变体就像它们的名字所说的那样，将你的智能设备变成砖块。有人已经厌倦了所有的物联网安全缺陷，并采取了极端(和非法)的措施来解决这个问题。一些早期报告来自一家名为 Radware 的安全公司，他们在他们的蜜罐中分离出了两种病毒变种。

简而言之，BrickerBot 通过使用暴力获得了对不安全的基于 Linux 的系统的访问权。它尝试使用通用默认根用户名/密码对进行 telnet 登录。一旦进入，它就使用 shell 命令(通常由 BusyBox 提供)将随机数据写入任何挂载的驱动器。这很容易

```
dd if=/dev/urandom of=/dev/sda1
```

随着二级存储被擦除，该设备实际上是无用的。这种攻击已经有了一个名称:永久拒绝服务(PDoS)攻击。

现在，任何带有 Hackaday 读卡器的卡都知道，像这样被关闭的系统可以通过 USB、JTAG、SD 和其他方法重新刷新来恢复。然而，我们不是 BrickerBot 的目标观众。我们都改变了设备的默认密码，对吗？对吗？

要了解更多物联网安全，请查看 [Elliot 今年早些时候关于僵尸网络的精彩文章](http://hackaday.com/2016/09/26/extra-large-denial-of-service-attack-uses-dvrs-webcams/)，以及[的后续文章](http://hackaday.com/2016/09/29/distributed-censorship-or-extortion-the-iot-vs-brian-krebs/)。