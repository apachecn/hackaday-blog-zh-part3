# 琢磨出一个 80 年代的益智玩具

> 原文：<https://hackaday.com/2016/06/29/puzzling-out-an-80s-puzzle-toy/>

[Ido Gendel]回顾上世纪 80 年代，孩子们通过回答“我的老师”或“西尔斯问答游戏”上的问题来学习。这个玩具有点令人费解。它怎么知道哪些答案是正确的。任何类型的芯片内存都不是那种你会扫进垃圾箱的东西，如果你有像现在这样的额外功能的话；它很贵。

为了使用该玩具，儿童将把笔记本放在设备上的塑料框架中。他们会打开有他们想参加的测验的那一页。左上角印着三个彩色方块。这个装置上有一组相配的彩色按钮。他们从上到下依次按下相应的按钮，然后机器就会神奇地知道测验中哪些答案是正确的。

我想知道机器是如何处理这些信息的。所有 27 种可能的代码是否有一个内部表？它以某种方式生成了答案表吗？他坐下来，手里拿着一张电子表格，左边是笔记本代码，右边是相应的正确答案。接下来，他盯着这些数字。

他最终确定有一种模式。这台机器使用彩色方块作为一个函数的输入，这个函数决定答案是什么。一张表本来只占 68 字节，但由于板上有一个 80 年代的芯片，要播放声音，要开关灯，这台机器需要所有它能得到的自由空间。