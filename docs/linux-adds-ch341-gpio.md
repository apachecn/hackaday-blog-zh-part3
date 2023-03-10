# Linux 增加了 CH341 GPIO

> 原文：<https://hackaday.com/2018/02/21/linux-adds-ch341-gpio/>

曾经有一段时间，USB 转串行硬件意味着一家公司:FTDI。但今天有相当多的选择，其中最常见的是 WCH CH341。Linux 对这些芯片的支持已经有一段时间了，但只是用作通信端口。该器件实际上有 RS232、I2C、SPI 和 8 个通用 I/O (GPIO)引脚。[ZooBaB]采用了一个公开 GPIO 的[树外驱动程序，并让它与一些看起来可怕的 CH341 板](http://www.zoobab.com/ch341-usb-spi-i2c-uart-isp-dongle)一起工作。

他必须对驱动程序进行轻微的修改才能在/sys/class/gpio 中获得六个 gpio。不过，一旦到了那里，就很容易使用 shell 脚本或任何可以写入对应于 GPIO 管脚的虚拟文件的东西来操纵管脚。

例如，他做了一个简单的速度测试:

```
#!/bin/bash
x=100000
while ((x--)); do
 i=$((i+1))
 echo 0 > /sys/class/gpio/gpio1/value
 echo 1 > /sys/class/gpio/gpio1/value
done
```

他从输出引脚获得了大约 2.2 kHz，虽然他没有说确切的硬件配置，但它可以让您了解可能的速度。

还有一些其他的例子，以及一些暴露 I/O 引脚的廉价电路板。也有一些关于那些板的一些模型的讨论。

共享和破解驱动程序的能力是 Linux 对黑客如此重要的原因之一。您的 Linux 系统可能有您需要的所有工具，如果没有，它们是一个软件包管理器命令。即使你不喜欢构建一个完整的驱动程序，像 ZooBab 那样修补一个也是非常可行的。

当然，还有更快的方法来驱动 I/O。我们在 2014 年查看了 [CH340 和 CH341](https://hackaday.com/2014/12/02/finding-a-cheaper-usb-to-serial-chips/) 的细节。