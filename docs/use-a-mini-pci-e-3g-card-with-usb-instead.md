# 请改用带 USB 的迷你 PCI-e 3G 卡

> 原文：<https://hackaday.com/2017/03/29/use-a-mini-pci-e-3g-card-with-usb-instead/>

早在 2000 年代末，当上网本成为最新的时尚时，一些型号会带有内置的 3G 调制解调器用于互联网接入。在那个时候，真正的移动互联网也是一件很酷的事情——远远领先于被称为 WAP 的虚假先知。这些调制解调器通常会插入上网本主板上的迷你 PCI-e 插槽中。[【delokaver】想出了如何通过 USB 而不是](http://www.instructables.com/id/Running-mini-PCI-e-3G-card-with-USB-mini-PCI-e-t/?ALLSTEPS)使用这些 3G 卡。

这实际上是一个相当简单的方法。Mini PCI-e 标准有一对专用于 USB 数据线的引脚，调制解调器使用这些引脚与主机进行通信。不幸的是，这不像在四线 USB 电缆上焊接那么简单。调制解调器依靠 Mini PCI-e 插槽的 3.3V 电源，而不是 USB 的 5V 电源。没问题，只要得到一个低压差 3.3V 稳压器，并运行它的 USB 端口。然后，这是一个足够简单的问题，找出哪些引脚用于与 SIM 卡通话，并将它们焊接到 SIM 卡适配器上，或者直接焊接到卡本身，如果你愿意的话。该指南涵盖了单一型号的 3G 调制解调器，但很可能大多数都使用非常相似的设置，所以不要害怕自己尝试一下。

总的来说，Mini PCI-e 是一个相当不受欢迎的接口，但我们以前见过这种攻击的反面，[一个 Mini PCI-e 到 USB 的适配器，用于为笔记本电脑添加 12 轴传感器。](https://hackaday.com/2013/01/31/12-axis-sensor-adds-auto-screen-orientation-to-this-older-tablet-pc/)

【感谢 Itay 的提示！]