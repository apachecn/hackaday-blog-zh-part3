# 新零件日:真正安全的工作站

> 原文：<https://hackaday.com/2016/09/19/new-part-day-a-truly-secure-workstation/>

每个现代计算设备中都有一个信任链，从您自己编写的代码开始，向后延伸到您正在使用的任何框架、任何操作系统、任何驱动程序，最终是您正在运行的任何 BIOS、UEFI、安全引导或固件。借助英特尔处理器，这一信任链延伸至英特尔管理引擎，这是一个独立于 CPU 运行的系统，可以访问网络、USB 端口和计算机中的所有其他设备。

不用说，这种信任链是站不住脚的。任何对计算机中运行的每一行代码进行审计的尝试都只会遇到挫折。没有一台基于英特尔的现代计算机是完全开源的，也没有一台计算机可以被验证是安全的。AMD 也一样糟糕，最近创建开放计算平台的尝试也遭遇了挫折。[Bunnie]的 [Novena 笔记本电脑接近了](http://hackaday.com/2014/04/02/bunnie-launches-the-novena-open-laptop/#more-118832)，但是像任何工程任务一样，设计 Novena 是一项折衷的工作。你可以避开现代 BIOS，coreboot 仍然使用二进制 blobs，Libreboot *暂时不会在 Hackaday 上讨论。*没有现代的、完全开放的、完全安全的计算平台。他们都不可信。

来自猛禽工程公司的 [Talos 安全工作站](https://www.raptorengineering.com/TALOS/prerelease.php)，一个[即将到来的群体供应活动](https://www.crowdsupply.com/raptorcs/talos)是现代计算不可信的答案。Talos 致力于创建世界上第一个 libre 工作站。这是一个 ATX 兼容的主板，是完全可审计的，从原理图到固件，没有任何二进制斑点。

### RISC 架构将会改变一切。

“安全”这个词不会和现代英特尔处理器联系在一起，AMD 也一样糟糕。大多数 ARM 处理器都过时了，因为即使处理器没有绑定在 NDAs 中，也会有二进制 blobs 四处浮动。即使是图形也很难做到安全，虽然开源 GPU 存在，但它们并不完全是强大的。

要使计算机完全安全，你必须走出通常的体系结构，而且安全计算机的市场根本不存在保证一个全新的体系结构。对于 Talos，Raptor Engineering 选择了 IBM 的 POWER8 处理器。这种架构现在在计算领域最常见，价格标签上比 Microcenter 提供的多几个零，但从历史上看，电源线可以追溯到 CELL 处理器、GameCube 和[Zero Cool]的 sweet clear 笔记本电脑。

其余硬件包括 8 个支持 256GB 内存的 DDR3 插槽、2 个 x16 PCIe 插槽、4 个 x8 PCIe 插槽、1 个传统 PCI 插槽、1 个内部 mPCIe 插槽、8 个内部 SATA 6Gb 端口、2 个外部 eSATA 6Gb 端口、1 个 HDMI 端口、8 个 USB 3.0 端口、2 个外部和 2 个内部 RS232 端口以及 1 个内部 GPIO 接头。规格和支持的操作系统的完整列表可在 [Raptor 工程网站](https://www.raptorengineering.com/TALOS/prerelease_specs.php)上获得。

应该注意的是，这不是唯一可用的 POWER8 主板。Tyan 生产了一个 POWER8 服务器主板，虽然它不像 Talos 那样开放。即使有了 Talos，它的开放和安全程度也有一些限制；多亏了 NDAs，一些 PCIe 子系统是不可审计的。

虽然众包供应活动尚未启动，但我们知道配备 8 核 130 瓦 TDP POWER8 CPU 的入门级 Talos 系统的价格将在 5300 美元左右。根据 Raptor Engineering 的说法，一个独立的无板 CPU 的价格大约为 4000 美元。这很贵，但对于高性能企业工作站来说并不可怕。你在这里为安全性和可审计性付费，我们希望 Talos 是成功的，哪怕只是为了证明真正安全的计算是有市场的。