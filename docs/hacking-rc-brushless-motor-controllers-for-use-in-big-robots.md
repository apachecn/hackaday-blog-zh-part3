# 用于大型机器人的遥控无刷电机控制器

> 原文：<https://hackaday.com/2016/05/18/hacking-rc-brushless-motor-controllers-for-use-in-big-robots/>

churlz 教授]写信让我们知道他的结果，修改无线电控制 ESC(电子速度控制器)用于大型(250 磅范围)战斗机器人的传动系统。这是一个非常长且复杂的构建日志条目，充满了细节和背景。

如果你想让某样东西转得又快又硬，无刷就是你想要的。与有刷 DC 电机相比，无刷电机提供了更好的功率重量比，但有些应用——如大型机器人的传动系统——不如其他应用简单。最大的问题之一是控制。廉价的无刷电机很有前途，但正如[丘尔兹教授]所说，“业余爱好电机控制设备不太适合这项任务。这些控制器通常是为模型飞机制造的，制造很轻，使用不切实际的方法评估部件的寿命，通常没有反转功能，也没有在低速和接近失速的情况下保持扭矩的能力，而这正是 DC 汽车公司的亮点。“考虑到一个 243 磅的机器人**的惯性也是一个因素——控制器和电机想立即开始移动，但另一边的重型机器人却不想。答案是混合了硬件和固件的调整以及大量的测试。**

 **构建日志充满了有趣的事情，包括机器人的传动装置和其他机械细节，但为了获得无刷电机传动系统之旅的要点，有一部分是什么导致[丘尔兹教授]思考[无刷电机——在小机器人中取得了不同程度的成功——是否会扩大到大约 250 磅的机器人](http://www.etotheipiplusone.net/?p=3985#2),关于[测试和调查他选择的电机和控制器的细节](http://www.etotheipiplusone.net/?p=3985#5),最后是[对他的结论的总结](http://www.etotheipiplusone.net/?p=3985#7)。最后他发现这是一次有限的成功。

无刷电机控制是许多人非常感兴趣的领域。churlz 教授]利用了[tgy——一种用于修改基于 ATMega 的电子稳定控制系统固件的开源工具](https://github.com/sim-/tgy),那些发现中国廉价电子速度控制器(ESC)能力不足的人[设计了他们自己的开源电子稳定控制系统](http://hackaday.com/2016/02/04/adding-position-control-to-an-open-source-brushless-motor-driver/)。

这里有一个视频，展示了战斗机器人使用无刷电机和改进型电子稳定控制系统的一些最终测试。马达的性能不是很直观，但看着它作为虚拟对手攻击一个无助的硬件仍然很有趣。

 [https://www.youtube.com/embed/wKQ4r96IIgE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/wKQ4r96IIgE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

**