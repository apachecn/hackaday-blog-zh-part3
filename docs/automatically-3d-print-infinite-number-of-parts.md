# 自动 3D 打印无限数量的零件

> 原文：<https://hackaday.com/2017/09/15/automatically-3d-print-infinite-number-of-parts/>

我们已经看到 3D 打印机有无限的生产量，包括一些专利申请的尝试，这可能会也可能不会阻止它们的发展。绕过争议的一个方法是用一种完全不同的方式去做。[Aad van der Geest]的解决方案可能无法让您打印无限长的零件，但它将允许您打印无限数量的相同或不同的零件，至少直到您的卷轴用完。

[Aad]的解决方案是在进入下一个之前，让[刀片自动从印刷床上移除每个零件。为此，他组装了一个轨道系统，放在 Ultimaker 2 的床上，但不在外围。一端的伺服系统沿着轨道拉动刀片，扫过床，并将床上的任何部分移动到一端，在那里它们脱落。这一切都是通过特殊的 g 代码和围绕一个](https://www.thingiverse.com/thing:2526792) [PIC12F629](http://www.microchip.com/wwwproducts/en/PIC12F629) 构建的电路的组合来完成的。

我们认为非常聪明且有趣的事情之一是，在零件完成后，挤出机移动到打印机的顶部角落，并按下微型开关，告诉 PIC12F629 开始零件移除过程。你可以在下面的第一个视频中看到这一点。g 代码在可配置的暂停后再次接管。

但是[Aad]增加的功能不止这些。如下面的第二个视频所示，从构建板上刮下零件后，挤出机上的一个销钉用于提升和放下刀片几次，以移除倾向于留在刀片上的小零件。此外，通过在小脊上移动几次，挤出机在印刷之间被净化。这当然也包含在特殊的 g 代码中。

既然很明显 g 代码还必须包含要打印的零件，那么如何生成特殊的 g 代码呢？为此[Aad]写了一个名为 gcmerge 的 Windows 程序。它读取您编辑的配置文件，该文件包含:包含零件 g 代码的文件列表、打印数量、是否希望在打印之间清洗挤出机、各种挤出机温度、冷却时间等。你可以在 [hackaday.io 页面](https://hackaday.io/project/27251-automatic-part-unloader-for-3d-printer)上找到所有这些，以及 gcmerge 程序的源代码。顺便说一下，您也可以在那里找到 PIC12F629 代码。

 [https://www.youtube.com/embed/xMVE7-IOp78?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xMVE7-IOp78?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/ES5mVhNC44E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ES5mVhNC44E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



至于那些带有传送带式打印床的无限生产量打印机，我们首先是在看到[Bill Steele]的一台打印机后提出来的，他在 MakerBot 上添加了一条 45 度角的传送带。然后我们看到 BlackBelt 推出了自己的[，可以打印非常长的对象](https://hackaday.com/2017/05/12/another-printer-with-an-infinite-build-volume/)，比 build plate 长得多。但是这些无限容量打印机也不是没有专利争议。