# E3D 推出换刀 3D 打印机

> 原文：<https://hackaday.com/2018/03/24/e3d-introduces-tool-changing-3d-printer/>

E3D 在本周末的中西部 RepRap 节上介绍了他们对多材料印刷的最新解决方案。他们对具有更换工具架能力的 3D 打印机的研究项目是多材料打印的最新进展。这是一个工程天才的作品，[他们已经写下了他们的拆卸过程，这一切是如何发生的。](https://e3d-online.com/blog/2018/03/21/tool-changer-q)

虽然铣床和其他花哨的工业 CNC 已经进行了几十年的刀具更换，并且 RepRap 社区也研究了几年，但它真的没有流行起来。那么问题是，在 3D 打印机上更换工具有什么好处？答案是多材料打印，并且以一种没有当前多材料打印方法的缺点的方式来做。

目前有三种印刷多种材料的方法。第一种是将两个喷嘴放在同一个挤出机上，但这有一个喷嘴干扰另一个喷嘴的缺点。第二种是将两种不同的塑料通过同一个喷嘴，比如 E3D 的独眼巨人，或者普鲁萨的多材料升级版。这有交叉污染的缺点，你不能打印需要不同温度分布的材料。第三种方法是简单地在同一台机器上使用多个托架，例如 Autodesk 的可爱的东西或 [Project Escher](https://hackaday.com/2017/01/08/ces2017-really-fast-3d-printing-for-large-builds/) 。最后一种方法极其复杂。

多材料印刷问题的答案是热插拔工具头，但要做到这一点，你需要精度和可重复性。E3D 的人已经在这方面研究了很多年，我记得几年前看到过一些关于电永磁体的实验，但是现在他们终于有了解决方案。答案很简单，就是一个由廉价的业余爱好伺服转动的凸轮。这是一种运动学耦合，允许托架以 5 微米的精度夹紧到工具架上。

现在，E3D 在刀具更换 3D 打印机方面的实验已经在一台 3D 打印机中达到高潮，该打印机具有刀具更换托架、四个工具架、一些令人惊叹的线性轨道和 CoreXY 配置。这台打印机打印出来的照片非常壮观。有四种颜色的长椅，遥控汽车的传动系统，齿轮用陶尔曼塑料印刷，驱动轴用 ABS 印刷。这辆车是由多个旅馆制作的单个印刷品，证明了多材料印刷的大部分问题随着 E3D 交换工具头印刷机而消失。

 [![The cam-lock mechanism on the carriage](img/65791c94696bb6fa3a16339176901a72.png "IMG_20180323_184101")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/03/img_20180323_184101.jpg?ssl=1) The cam-lock mechanism on the carriage [![Cam-lock mechanism](img/6272996eda43605cb3cca46efc1605a0.png "IMG_20180323_183843")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/03/img_20180323_183843.jpg?ssl=1) Cam-lock mechanism [![toolheads](img/462c882c86143385ff2875c8ba642b2c.png "IMG_20180323_183853")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/03/img_20180323_183853.jpg?ssl=1) toolheads [![two-color multimaterial print](img/7cbcf07efd789edd0814e1efec63ab1d.png "IMG_20180323_184831")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/03/img_20180323_184831.jpg?ssl=1) two-color multimaterial print [![four-color benchy](img/31b9894523aea769e7d5aa442517d361.png "IMG_20180323_184704")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/03/img_20180323_184704.jpg?ssl=1) four-color benchy [![Cute Kracken](img/9bb8d9472b56b0ef91eedeefce533042.png "IMG_20180323_184712")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/03/img_20180323_184712.jpg?ssl=1) Cute Kracken

如果你有兴趣购买这些打印机中的一台，E3D 目前有[一项针对潜在买家的调查](https://docs.google.com/forms/d/e/1FAIpQLSdLJFf7Qgp_7iPsPcWK_wog66XA79qKFwFKHRXwfiZ3X9uRXA/viewform)和[一个为任何未来购买的存款队列](http://e3d-online.com/tool-changer-join-the-queue)。