# MeatBagPnP 让你自动选择和放置

> 原文：<https://hackaday.com/2017/11/29/meatbagpnp-makes-you-the-automatic-pick-and-place/>

令人惊讶的是，如今黑客们是如何用像沙粒一样小的 SMD 部件来构建日益复杂的硬件的。获得用于原型制作的小批量多层 PCB 和焊接模板比以往任何时候都更容易。但是取放——取零件并把它们塞在 PCB 上准备焊接的过程——是难以捉摸的，原因有几个。首先，它只有在你计划进行批量生产时才有意义，因为设置小型 PnP 机器的成本和时间是令人望而却步的。桌面 PnP 机还没有 3D 打印机普遍。将零件放置在电路板上是一个仍然需要手动完成的过程。只是确保你做的时候不要打喷嚏。

当然，人类是这个过程中缓慢的一部分。[Colin O'Flynn]写了一个 python 脚本，他称之为 [MeatBagPnP](https://github.com/colinoflynn/MeatBagPnP) 来缓解这个瓶颈。它旨在查看由 EDA 程序生成的器件位置文件中的一行，并在电路板上需要放置该器件的地方突出显示。然后人类做机器人 PnP 会做的事情。

条形码扫描仪不是必须的，但是使用它确实会使这个过程更快一些。当您扫描零件包上的代码时，脚本会高亮显示电子表格上的行，并在板上的第一个实例上放置一个标记。放置零件后，按空格键会在相同值的下一个实例上放置一个标记。该脚本显示，在相同值的所有部分都被填充后，它就完成了，然后您可以继续下一部分。如果你手边没有条形码扫描仪，你可以手动突出显示一行，它会告诉你把那部分放在哪里。看看下面的视频吧。

当然，在使用这个工具之前，你需要做一些准备。你需要一个好的 PNG 图像的董事会(双面，如果是双面)缩放，使其与目标董事会的尺寸相同。从 EDA 工具生成的器件位置文件必须使用电路板的左下角作为原点。然后你告诉工具电路板的尺寸，它会放大所有的尺寸，这样它就可以把红色标记放在指定的 XY 位置。该脚本适用于单面板和双面板。对于只有几个部件的电路板，这样做可能不值得，但是如果您试图手动填充一个有很多部件的复杂电路板，使用这样的脚本可以减少这个过程的痛苦。

该项目仍然是新鲜和粗糙的边缘，所以如果你有意见或反馈提供，[科林]正在倾听。

[Colin]的名字应该听起来很耳熟——他是构建了[chip whisper](https://hackaday.io/project/956-chipwhisperer-security-research)的黑客，该软件获得了 2014 年 T2 黑客日奖的二等奖。MeatBagPnP 项目是人工构建日益复杂的电路板并试图简化这一过程的结果。除了在休息后演练脚本如何工作，我们还嵌入了他三年前的另一个视频，当时他正在[填充零件——包括 BGA 的零件——然后用破解的固件在中国的烤箱里回流。](https://hackaday.com/2016/01/03/bga-hand-soldering-video/)

 [https://www.youtube.com/embed/3arWSPCR0Ww?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3arWSPCR0Ww?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/-DMYJmB4naA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-DMYJmB4naA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

