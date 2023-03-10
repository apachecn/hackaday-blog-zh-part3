# 施乐 Alto CRTs 需要一个小灯泡才能工作

> 原文：<https://hackaday.com/2017/10/15/xero-alto-crts-needed-a-tiny-lightbulb-to-function/>

在现实世界中，组件并不像我们想象的那样工作。导线有电阻，电阻有电感，电容有电阻。然而，一些设计师喜欢利用这些不完美，这是我们的老朋友[Ken Shirriff]在修复施乐 Alto 的 CRT 时注意到的。

[Ken]试图将施乐显示器连接到 Alto 上，因为它几乎和 Alto 一样旧，所以他对它不能工作并不感到惊讶。然而，令他惊讶的是，当他关掉显示器时，一个完美的画面出现了，就在关机的一瞬间。那是什么意思？

请记住，这是一个 CRT 设备。因此，完美的图像意味着垂直和水平扫描的频率都正确。这也意味着你有高电压和驱动电子枪。如果你太年轻，记不住所有这些内容，[Ken]会在他的帖子中详细介绍。

他发现 CRT 栅极电压在运行期间不存在。电压来自高压电源，但神秘的是，高压是正常的。在电网电压电路中有一个小灯泡。一个 28V 的设备，就像一个手电筒的灯泡。它打开了，结果是因为一根导线断了。修理灯泡上的坏掉的引线后，监视器又可以工作了。

在纸上，当你给灯泡通电时，它就会亮起来。在现实生活中，情况要复杂一些。白炽灯丝开始时几乎完全短路，在非常短的时间内消耗大量电流。当电流流动时，灯丝变热，电阻上升。这降低了电流消耗。这种效应被称为浪涌电流，是试图用晶体管或其他电子开关打开灯泡的设计师的灾难。

然而，不知名的施乐电源设计者利用这种效应作为电流限制器。600 伏的短脉冲几乎不会注意到灯泡，但如果电流过大或时间过长，灯泡的电阻就会上升，从而阻止太多的电流流过太长时间。当灯泡打开时，负亮度的栅极为电子提供了一个不可逾越的屏障。显然，亮度网格比电路的其他部分更早失去电力，并且在它不碍事的情况下——或者说，部分不碍事——图像是好的，直到电路的其他部分也失去电力。

今年早些时候，我们看到了[【Ken】在这台机器](https://hackaday.com/2016/06/26/restoring-the-groundbreaking-xerox-alto/)上所做的努力。顺便说一句，灯泡并不是唯一一种[对某些刺激做出反应而改变电阻的东西](https://hackaday.com/2016/09/27/variable-resistors-controlled-by-the-environment/)。你可能会喜欢施乐公司 1972 年的广告，宣传 Alto 能够完成电子邮件和打印等高级任务。

 [https://www.youtube.com/embed/tjvSWCQVpJ0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/tjvSWCQVpJ0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

