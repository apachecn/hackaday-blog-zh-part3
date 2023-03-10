# 对水晶收音机越来越认真

> 原文：<https://hackaday.com/2016/04/07/getting-serious-about-crystal-radios/>

水晶收音机是一种永恒的学习体验，通常是我们对收音机工作原理的第一次了解。对我们中的一些人来说，童年的魅力永远不会消失。以吉姆·库什曼(Jim Cushman)为例，这家伙喜欢做老式踏板车、摩托车，尤其是[水晶收音机](http://www.hobbytech.com/crystalradio/crystalradio.htm)(特别感谢线圈缠绕爱好者伙伴[m·罗森](http://martinos.org/lab/lfi)提供链接)。深入挖掘，我们发现一个致力于水晶收音机设计的完整社区。在这篇文章中，我们将回到基础，研究无线电接收机设计的基础。

## 工作原理:

一个[晶体收音机](http://makearadio.com/crystal/crystal-schematics.php)基本上是一个连接到天线和包络检波器的高 Q 谐振器。如今，包络检波器是一个点接触二极管，如 1N34 锗二极管。

![cs09-schematic](img/061f857e48947d0048f4a1cabdfe4371.png)

谐振电路通过特定的波长(或者更具体地，取决于其 Q 的波长范围)。二极管检测器提供该波长内信号的振幅或包络。高阻抗或高灵敏度耳机将此包络转换为您可以听到的声音信号。

晶体收音机的巧妙之处在于没有使用有源射频放大器。收音机由调谐到的输入无线电信号供电。更复杂的晶振组可能有一个以上的调谐级，可能有 3 或 4 个，以最大限度地减少接收器带宽，实现最大的灵敏度和选择性。

## 历史课:

泰坦尼克号马可尼室的娱乐

![5598021](img/76e788d9b977945a84123ad2a3f1f4cc.png)

【来源:】antiquewireless.org

泰坦尼克号马可尼站上使用的主要接收器基本上是一个三级晶体收音机，只是它使用了一个[磁性探测器](http://www.sparkmuseum.com/MAGGIE.HTM)而不是半导体。此处显示了该站控制/接收室的精确 3D 效果图，主接收器位于桌子中间，磁检测器直接位于其上方，用螺栓固定在墙上，备用发射器位于右侧。

关于泰坦尼克号无线电系统的最佳分析只能在纸质文件中找到，Eric P. Wenaas，“泰坦尼克号的无线设备:纪念概述。”[古董无线协会评论](http://www.antiquewireless.org/uploads/1/6/1/2/16129770/review_index_file_pdf.pdf)，2012 年第 25 卷。

## 晶体无线电设计的先进概念；

像泰坦尼克号和其他早期的无线接收器一样，吉姆自己缠绕线圈，使用木头外壳和点对点线路。通过大量使用[李兹线](https://en.wikipedia.org/wiki/Litz_wire)来最大化 Q 值，吉姆在水晶收音机上创造了许多变体，所有这些都显示在[的页面](http://www.hobbytech.com/crystalradio/crystalradio.htm)上。

 [![Crystal Set with FET Front](img/2ab6770a85e1dfd5bd23222972d07287.png "Crystal Set with FET Front")](https://hackaday.com/2016/04/07/getting-serious-about-crystal-radios/crystal-set-with-fet-front/) Crystal Set with FET Front [![Crystal Set with FET top](img/c9d1eab45e3b21f80c890f75706bb62a.png "Crystal Set with FET top")](https://hackaday.com/2016/04/07/getting-serious-about-crystal-radios/crystal-set-with-fet-top/) Crystal Set with FET top [![Beacon Front](img/a88065665dd98b038fb5374820d1302a.png "Beacon Front")](https://hackaday.com/2016/04/07/getting-serious-about-crystal-radios/beacon-front/) Beacon Front [![Beacon Rear](img/1d8ba7c81b656c12811cf36a019ae3dd.png "Beacon Rear")](https://hackaday.com/2016/04/07/getting-serious-about-crystal-radios/beacon-rear/) Beacon Rear

Jim 甚至为其中一些收音机起了名字，例如作为套件提供的“hobbydyne”接收器。

 [![2nd gen Hobbytech Rear](img/18425082b9cd2e37442a9d7cbc900dc7.png "2nd gen Hobbytech Rear")](https://hackaday.com/2016/04/07/getting-serious-about-crystal-radios/2nd-gen-hobbytech-rear/) 2nd gen Hobbytech Rear [![2nd gen Hobbytech front](img/1a060dc1b6be75eb39f564dda20b53bc.png "2nd gen Hobbytech front")](https://hackaday.com/2016/04/07/getting-serious-about-crystal-radios/2nd-gen-hobbytech-front/) 2nd gen Hobbytech front

## 还有更多:

Jim 不是唯一的一个，有一个水晶收音机设计者的社区，他们大部分工作的视频通过快速搜索显示出来。

 [https://www.youtube.com/embed/_ID4qYysXyI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_ID4qYysXyI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



您甚至可以添加一个 BFO 来复制 CW 和 SSB(这可以将您的晶振变成一个直接变频接收机，检波器二极管变成您的混频器):

 [https://www.youtube.com/embed/9-LJpD0CoQw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/9-LJpD0CoQw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



## 去车库！

通过建造水晶装置来学习无处不在。一本来自东德的广播指南书，以水晶为特色。

回归基础，做一个水晶收音机。了解谐振电路，体验历史，缠绕高 Q 电感，制作天线，体验无线设计的基础知识。

### **作者简介:**

[Gregory L. Charvat](http://glcharvat.com/Dr._Gregory_L._Charvat_Projects/About.html) ，博士，喜欢研究旧技术，为 21 世纪的技术发展提供信息，是[Humatics corp .](http://site.humatics.com/)的首席技术官，[小型和短程雷达系统的作者，](http://www.amazon.com/Short-Range-Practical-Approaches-Electrical-Engineering/dp/143986599X)Hyperfine Research Inc .和 Butterfly Network Inc .(都在 4catalyzer)的联合创始人，电气工程的现代和实用方法系列图书的编辑，CNN、CBS、Sky News 等的客座评论员。作为麻省理工学院媒体实验室的访问科学家，他发明了飞行时间微波照相机。作为麻省理工学院林肯实验室的技术人员，他创建了一个穿墙雷达成像系统，该系统在 2010 年 MSS 三军雷达研讨会上获得了最佳论文，并且是麻省理工学院 Provost 办公室 2011 年的研究亮点。Greg 曾在麻省理工学院教授短期雷达课程，他的“构建小型雷达”课程是 2011 年排名第一的麻省理工学院专业教育课程，并被其他大学、实验室和私人组织广泛采用。