# 一个晶体管 RTL-SDR 上变频器

> 原文：<https://hackaday.com/2017/08/07/one-transistor-rtl-sdr-upconverter/>

即使你没有使用过，你可能已经看到了许多项目与廉价的 RTL-SDR USB 加密狗。dongle 最初是为电视使用而设计的，是一种软件定义的无线电，许多人将其重新用于各种无线电黑客项目。然而，有一个小问题。默认情况下，该设备只能在 50 MHz 左右的频率下工作。有一些方法可以改变这一点，但最干净的操作方法是添加一个上变频器，将所需频率调高。听起来很复杂？[Qrp-Gaijin]展示了如何用单个晶体管实现[。你可以在下面看到一些结果的视频。](http://qrp-gaijin.blogspot.co.nz/2017/07/rtl-sdr-upconversion-with-diode-ring_30.html)

事实上，[Qrp-Gaijin]构建了一个早期版本，但对性能不满意。他发现他最初的振荡器以基频驱动泛音晶体。该设备工作，但只是因为振荡器输出谐波，包括实际所需频率(49.8 MHz)的三次谐波。

改变振荡器拓扑结构达到了目的。调谐电路阻止振荡器在基频处具有足够的增益。他做了一些其他的调整，并且——根据帖子——他仍然有一些他想在未来改进的地方。

也有人努力改进 RTL-SDR 电路。如果你想看一个更复杂的上变频器，你可能想看一个基于电路模块的[。](https://hackaday.com/2012/07/08/adding-more-frequencies-to-you-software-defined-radio/)

 [https://www.youtube.com/embed/KebdfpLvGfI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/KebdfpLvGfI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/ZeMjytQTov0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZeMjytQTov0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

