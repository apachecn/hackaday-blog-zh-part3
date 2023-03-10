# IPhone 显微镜和其他冒险

> 原文：<https://hackaday.com/2016/04/11/iphone-microscopy-and-other-adventures/>

CMOS 成像芯片一直在稳步改进，其成本和性能受到竞争激烈的智能手机行业的推动。随着 CMOS 传感器变得越来越好，越来越便宜，黑客实验室项目对它们越来越感兴趣。在这篇文章中，我将展示一些高分辨率传感器的应用，这些传感器已经放在你的口袋里，或者放在你存放手机的任何地方。

## CMOS 与 CCD

首先，让我们快速回顾一下图像传感器。你可能是 CMOS 和 CCD 传感器的负责人，但是到底有什么区别呢？

![cddandcmos](img/bc9bccd4202dc7fc80fb5e6019fd2bb1.png)

CCD and CMOS imaging sensors: from [this](http://meroli.web.cern.ch/meroli/lecture_cmos_vs_ccd_pixel_sensor.html) excellent page at CERN.

如上图所示，CCD 和 CMOS 传感器基本上都是光电二极管阵列。击中芯片区域的光子被光电二极管转换成电荷。不同之处在于电荷是如何被推来推去的。CCD 传感器是模拟设备，电荷通过芯片转移到单个放大器。CMOS 传感器在每个单元中嵌入放大器，通常还包括片内模数转换，从而实现完整的“片上摄像头”解决方案。

因为 CMOS 传感器可以更快地放大信号并将其转移到数字域，所以它们可以使用更便宜的制造工艺，从而开发出成本更低的成像芯片。然而，传统上它们也有许多缺点，因为每个电池中包含更多的电路，留下来收集光的空间更少。由于使用了多个放大器，每个电池中的放大器之间的制造差异很小，因此很难获得一致的图像。直到最近，CMOS 传感器还被认为是低端选择。虽然 CCD 传感器(通常是大型冷却 CCD 传感器)仍然经常是预算较大的科学应用的首选，但 CMOS 传感器现在已经成为高性能 DSLRs 的发展方向。

## 成像 DNA

![phonescope](img/e79e0685e8cc155ea6431a2a8f378b23.png)

Figure 2 from the [paper](http://pubs.acs.org/doi/abs/10.1021/nn505821y). Insets b,d, and f show single fragments of DNA (lambda phage) imaged using an mobile phone.

不过，看看 CMOS 传感器能做多少事情总是很有趣。最近的一篇文章描述了使用手机摄像头对拉伸在表面上的单个 DNA 分子进行成像。当你考虑到每个碎片只有 10 微米长(0.01 毫米)时，这些结果是非常令人印象深刻的。研究人员 3D 打印了手机的附件，其中包括蓝色激发激光。这种激光被用来照射在一个表面上伸展开来并用荧光染料染色的 DNA。当被照亮时，染料发出绿光，并通过过滤器和放大镜被手机摄像头检测到。

虽然这是一个极端，但其他人已经建议使用廉价的基于手机的显微镜进行病原体检测，廉价的基于手机的荧光显微镜将成为一个整洁的黑客工具(我知道许多人正在考虑启动这样一个项目，所以如果你感兴趣，请在下面留下评论！).

## 通用显微镜

![echolabs](img/bc592d09979c32f220b40f7e90719a0c.png)

The Echolabs wooden microscope.

然而，如果你对荧光不太感兴趣，而对通用廉价显微镜更感兴趣，还有很多其他选择。受到 Kurt 关于他的 Echolabs 手机显微镜的[帖子](http://nic.ucsf.edu/blog/?p=1611)的启发，我一直在玩他的和其他基于手机的显微镜。

我相信 Echolabs 显微镜最初是在贸易展上免费赠送的。然而，它现在可以从他们的网站上以 10 美元的价格买到。显微镜是一个扁平包装的激光切割套件。虽然组装可能有点复杂，但有一个很棒的组装视频，应该不会超过 15 分钟左右。

这个项目非常有趣，绝对是一个有趣的项目，但是它作为显微镜的性能有多好。为了对此进行研究，Kurt 引入了 [USAF1951 分辨率目标](https://en.wikipedia.org/wiki/1951_USAF_resolution_test_chart)。USAF1951 目标是一张幻灯片，上面标有不断缩小的特征。我从 [Thorlabs](http://www.thorlabs.de/newgrouppage9.cfm?objectgroup_id=4338) 那里拿到了我的。

此目标允许您确定显微镜可以分辨的最小特征。有点讽刺的是，这个目标会比 Echolabs 显微镜贵很多倍，但是如果你对这些东西感兴趣，这是一个有用的校准标准。

我用木制显微镜获得的图像显示在左边。这是 USAF1951 的内部目标集，向下第一层。像库尔特一样，我也能分辨出第 5 组的第 2 个元素。这里的每条线都是 36 微米厚(0.036 毫米)。10 美元还不错！

 [![The USAF1951 captured using the Echolabs wooden microscope and an iPhone 6S.](img/75b9478e6cc0e4e3487d3ae66a399765.png "echolabs_usaf1951")](https://hackaday.com/2016/04/11/iphone-microscopy-and-other-adventures/echolabs_usaf1951/) The USAF1951 captured using the Echolabs wooden microscope and an iPhone 6S. [![The same region imaged using an Olloclip x21 Macro lens (Macro Pro lens)](img/a96964d0d4c9a9a8c40e44897bac784d.png "olloclop_usaf1951")](https://hackaday.com/2016/04/11/iphone-microscopy-and-other-adventures/olloclop_usaf1951/) The same region imaged using an Olloclip x21 Macro lens (Macro Pro lens)

心血来潮，希望有一个可以随身携带的小型检查放大镜，我还拿起了一个 [Olloclip 微距专业镜头](https://www.olloclip.com/shop/lenses/macro-pro/)。虽然我可以隐约听到“这不是黑客”的低沉叫声，但一个好的检查放大镜是一个无价的黑客工具。我还认为它会有兴趣看看它在 USAF1951 上的表现。

右上方的图像显示了 iPhone 6S 上用这个镜头拍摄的 USAF1951 目标。虽然比 Echolabs 显微镜贵得多，但 Olloclip 表明 iPhone 的光学系统还可以更进一步。第 5 组的所有元素都清晰可见，如果放大，第 6 组的第 2 个元素也能清晰可见。这是大约 7 微米(0.007 毫米)的线宽。Olloclip 更好的照明和改进的光学系统可能会有所帮助。

## 从传统显微镜中捕捉图像

![phoneclamp](img/28c0d99e6d3e09ec51076951f4d6341b.png)

Phone to objective clamp

虽然对微米级特征成像非常有趣，但我最常用的显微镜是一种通用检测显微镜，用于检测元件和 SMD 返工。我也经常想给一件工作拍一张快照，要么记录我的进步，要么强调错误。过去，为了拍照，我曾努力将手机贴在目镜上。令人惊讶的是，这种方法很有效，但这是一个复杂而笨拙的过程。

当我使用目镜 C 型转接环和来自深圳的便宜的 CCD 成像器时。结果不太理想，我经常只想快速拍照并上传。令人惊讶的是，有一些夹具可以使手机贴紧眼罩的过程更加牢固(尽管它们非常昂贵)。必须有一个 3D 打印的替代品。

尽管如此，经过一番摆弄后，这个夹子可以产生相当合理的图像。下图显示了 TQFP IC 上 0.8 毫米间距的引脚。

![IMG_0659](img/84910101ef7e9f911e19b301481fac99.png)![IMG_0655](img/c115e3a9da850d106940d431d18adad8.png)

希望这篇关于手机显微镜的简短评论能给你一些启发。我很乐意听到更多基于光学的黑客项目。你是如何使用旧手机的摄像头的？如果你知道任何很酷的项目，或者正在计划一个，请在下面评论！