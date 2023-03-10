# 双核、ARM 驱动的 Commodore 64

> 原文：<https://hackaday.com/2016/07/02/the-dual-core-arm-powered-commodore-64/>

没有什么 CPU 比 6502 和它的兄弟 6510、6507、6509 以及我们在 NES 称之为 CPU 的东西更好理解了。有了这么大量的文档，几乎可以做任何事情。想要一个分立的和不谨慎的 6502？肯定的事。这是 NMOS 的版本，虽然。想要一个仿真版本。当然可以。随着库将 6502 移植到每个平台，只剩下一个地方可去:将 6502 放在 Commodore 64 中。[把它也做成双核，这样我们就可以运行 CP/M](http://telmomoya.blogspot.com.ar/2016/06/dual-core-c64.html) 。

这一构建基于[telmomoya]的早期构建之一——在 [ARM Cortex M3](http://telmomoya.blogspot.com.ar/2016/06/c64-software-cored.html) 上运行的软核 6510。这个构建的灵感来自于运行在 Arduino 上的 6502 仿真器[，这让[telmomoya]想知道如果他连接一些外部 RAM、CIA 或 SID 会发生什么。在 Arduino 上做到这一点很难，但有一些 5 伏兼容的 ARM 芯片，加上几组 SRAM，[tel]很快就有了运行 EhBasic 的仿真 6502。](https://forum.arduino.cc/index.php?topic=193216.0)

在 ARM 芯片上运行仿真 6502 并不是什么新鲜事。使这个版本引人注目的是对 C64 主板的适应。由于[telmomoya]已经将数据和地址线拆分到 SRAMs 中，所以在 C64 上为 DIP40 CPU 插槽构建一个适配器并不需要太多额外的工作。一些 74 系列逻辑芯片使接口变得容易，经过一点焊接后，[telmomoya]有了一个由 ARM 芯片驱动的 Commodore 64。

如果你在模拟一个芯片，你可以模拟两个，有了 Commodore 64，这带来了一些有趣的可能性。C64 有一个 CP/M 盒式磁带，它包含一个 Z80 CPU，与 6510 共享数据和地址总线。这种盒式磁盘允许“玩具电脑”C64 运行“商业”CP/M 操作系统([和 Z80 使 Commodore 128 更酷](http://hackaday.com/2013/12/09/guest-post-the-real-story-of-hacking-together-the-commodore-c128/))。因为[telmomoya]已经在模拟一个 CPU，模拟一个*的第二个* CPU 并没有那么难。

这是一个非凡的构建，如果你想提高 VisiCalc 的速度，这是一个很好的选择。