# 激光测序仪使用 Arduino 启用超级显微镜！

> 原文：<https://hackaday.com/2016/08/15/laser-sequencer-uses-arduino-to-enable-super-microscope/>

![pcb](img/9373a6b742860f4f819c2c82e8ec638f.png)

[Philip]’s Laser control Arduino shield.

菲利普·尼科维奇已经在新南威尔士大学建造了激光测序仪。他的平台用于在他的荧光显微镜系统上进行激光激发排序。在[Philip]的案例中，这些系统被用于超分辨率显微镜，这打破了衍射极限，允许对尺寸仅为几纳米(百万分之一毫米)的结构进行成像。

使用他在 Eagle 设计的 Arduino 盾牌，[Philip]能够以不到商业平台一半的成本构建该系统。

控制系统是围绕右图所示的简单 Arduino shield 构建的，它使用简单的 74 系列逻辑向他的装备中使用的激光二极管发送 TTL 控制信号。Arduino 运行允许编程和执行激光发射序列的代码。

[Philip]还提供了一些脚本，展示了 Arduino 如何与开源的 micro manager 控制软件进行交互。

![NicoLase1500EnclosureRender](img/0ff955cc9ebe970f0722223f91d57b9c.png)

除了原理图，[Philip]还提供了系统中使用的外壳和支架的 STEP 文件和图纸以及详细的 BOM。

比这一切更有用的也许是他提供的全面的评论。这描述了决定的动机，例如使用铝而不是钢，因为铝能够更有效地传热，并且不使用热糊，因为会产生气体。

虽然我几乎可以听到“不是黑客”的呼声，但开源平台和工具在学术界越来越多的使用让我们充满了喜悦。感谢您的来信[Philip],我们期待将来听到更多关于您的激光系统的信息！