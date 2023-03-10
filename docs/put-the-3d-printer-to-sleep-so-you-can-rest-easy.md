# 让 3D 打印机进入睡眠状态，让您高枕无忧

> 原文：<https://hackaday.com/2018/05/29/put-the-3d-printer-to-sleep-so-you-can-rest-easy/>

此时，你可能已经听说了这条新闻:廉价的中国 3D 打印机有时会着火。现在，我们不能说我们对发现绝对桶底齿轮不是按照最高标准设计的感到震惊(必须在某些地方偷工减料)，但这并不能改变这样一个事实，即有成千上万的黑客和制造商拥有这些可疑的机器之一。仅仅把它们扔到路边不是黑客的方式，所以我们必须想办法充分利用发给我们的这手牌。

[![](img/655699c6f26ff97a9b0a462fe76f9bb5.png)](https://hackaday.com/wp-content/uploads/2018/05/3dsleep_detail.jpg) 在通宵打印时睁着一只眼睛(也许还有一个鼻孔)睡觉后，Hackaday.io 用户[TheGrim]想找到一种方法来确保他的 Alunar Anet A6 不会在不必要的情况下长时间开机。于是他想出了一个办法[用打印机自己的 endstop 开关检测打印是否完成，并切断电源](https://hackaday.io/project/158568-3d-printer-auto-off)。

这个想法很简单，但是真正的诀窍当然在于实现。通过在 Cura 的 g 代码末尾添加一个“Home”命令，[TheGrim]推断他可以使用 Y endstop 开关来确定打印是否已经完成。这只是一个读取开关状态并采取行动的问题。

在最基本的实现中，开关可用于控制电源交流侧的继电器。但是[TheGrim]不信任继电器，他想加入一些“智能”功能，所以他最终使用了一个 PIC 微控制器和两个 12 安培的三端双向可控硅开关。还有几个 led 和拨动开关作为用户界面，允许您启用和禁用自动关机，并获得有关系统的状态信息。

切断 PSU [的电源会阻止另一场可怕的火灾](https://hackaday.com/2018/03/18/3d-printer-halts-and-catches-fire-analysis-finds-a-surprising-culprit/)吗？值得商榷。但这肯定没什么坏处，如果这能让[TheGrim]对运行他的机器更有信心，那就这样吧。[我们仍然建议家里有 3D 打印机的人](https://hackaday.com/2016/12/07/dont-leave-3d-printers-unattended-they-can-catch-fire/)[复习一下消防安全知识](https://hackaday.com/2016/12/06/hack-safely-fire-safety-in-the-home-shop/)。