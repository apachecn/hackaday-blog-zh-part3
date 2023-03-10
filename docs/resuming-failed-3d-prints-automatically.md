# 自动恢复失败的 3D 打印

> 原文：<https://hackaday.com/2018/04/13/resuming-failed-3d-prints-automatically/>

如果停电了，你的 3D 打印机会怎么样？如果喷嘴堵塞会怎么样？如果你的灯丝断了，用完了，或者变成一盘意大利面，会怎么样？对于所有这些情况，打印失败，浪费塑料和时间。为了他的 Hackaday 奖参赛作品，[robert] [发明了一种微型设备，可以保存所有失败的打印作品](https://hackaday.io/project/28672-box-for-resume-3d-print-automatically)，而且它不需要电池或 UPS。

[robert]的盒子背后的想法是监控发送到打印机的所有 g 代码，并允许在失败后继续打印。设计非常简单——一端是 USB 迷你端口，另一端是 USB A 端口，中间是三个按钮。这个盒子记录了 g 代码，如果打印机发生故障，这个盒子将重新启动，允许您从任何 Z 位置继续打印。

[robert]已经在一些打印机上测试了这个盒子，包括 Prusa i3、Creality CR-10 和一直很受欢迎的 explodey Anet A8。该项目已经经历了一些硬件修订，当然，还有一个花哨的 3D 打印电路板外壳。这是一个伟大的项目，也是我们在今年的 Hackaday 奖中看到的更有趣的 3D 打印工具之一。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)