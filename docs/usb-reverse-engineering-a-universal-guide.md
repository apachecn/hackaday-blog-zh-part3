# USB 逆向工程:通用指南

> 原文：<https://hackaday.com/2018/05/25/usb-reverse-engineering-a-universal-guide/>

每个黑客都知道冒险进入兔子洞意味着什么。无论持续一个下午、一个月还是几十年，找到一个新的利基主题并探索它的发展方向对 Hackaday 读者来说都是一种熟悉的体验。

[Glenn ' dev alias ' Grant]自称是一名普通的兔子洞潜水者，他意识到在探索特定主题时，短期知识和精神状态可能会丢失。这一次，在[探索逆向工程 USB 设备](http://devalias.net/devalias/2018/05/13/usb-reverse-engineering-down-the-rabbit-hole/)的同时，【格伦】获得了最好的资源、信息和工具——为他未来的自己和他人。

他的指南非常全面，涵盖了硬件和软件的所有必要领域。在正式定义了一个 USB 系统之后，【Glenn】让我们参考【LinuxVoice】，一个俏皮的 [关于为 RC 汽车编写 linux USB 驱动的教程，用 Python](https://www.linuxvoice.com/drive-it-yourself-usb-car-6/) 。转到硬件，讨论了许多开源和商业选项，包括[good fet](https://store.hackaday.com/products/goodfet42)、FaceDancer 和 Daisho——一种基于 FPGA 的监控工具，用于分析 USB 3.0、HDMI 和千兆以太网。如果你只需要嗅探低速 USB，这里有一个漂亮的小[包嗅探器](https://hackaday.com/2017/07/25/hackaday-prize-entry-usb-packet-snooping/)来自去年的 Hackaday 奖。

这是一个信息丰富、结构清晰的指南，包括 TL；完美位置的 DR 部分。它对 LibUSB 和 PyUSB 给予了应有的肯定，甚至包括了 USB over IP 的资源。

如果你担心像 BadUSB 这样的 USB 黑客，也许你应该检查一下 good USB——一种用于 USB 设备的硬件防火墙。

标题图片:Ed g2s ( [CC-SA 3.0](https://commons.wikimedia.org/wiki/File:Type_A_USB_connector.jpg) )。