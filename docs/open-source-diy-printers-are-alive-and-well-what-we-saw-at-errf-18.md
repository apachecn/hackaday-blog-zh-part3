# 开源 DIY 打印机生机勃勃:我们在 ERRF 18 看到了什么

> 原文：<https://hackaday.com/2018/07/05/open-source-diy-printers-are-alive-and-well-what-we-saw-at-errf-18/>

如果你关注桌面 3D 打印机市场，你可能不会惊讶于在[首届东海岸说唱节(ERRF)](https://hackaday.com/2018/06/20/this-weekend-the-east-coast-reprap-festival/) 上展出的几乎所有 3D 打印机都是中国制造的。甚至 Printrbot 首席执行官 Brook Drumm 也不得不承认，今年他的公司可能会最终咬紧牙关，开始销售海外制造的品牌和定制打印机。

[![](img/5c672f91f0e75d41054dde1db3831f74.png)](https://hackaday.com/wp-content/uploads/2018/06/errfdiy_printrbot.jpg) 当你能以 200 美元买到一台像样的([但让我们搞清楚，不是很棒的](https://hackaday.com/2017/12/08/how-cheap-can-a-3d-printer-get-the-anet-a8/) ) 3D 打印机时，毫不奇怪，美国和欧洲制造商很难保持竞争力。但并不是每个人都被低价打印机所吸引。他们知道他们可以花几百美元买一台像样的打印机，但对他们来说这不是重点。一些黑客对设计和制造机器的兴趣不亚于(如果不是更大的话)用成品制造小塑料船。

对我们来说幸运的是，这些人也是这样的人，他们记录他们的构建，并在开源许可下将他们收集的所有信息和设计文件提供给其他人。这样的建设者体现了 RepRap 运动的真正精神，我们很高兴地报告，在进口打印机的海洋中，有几个有趣的自制开源打印机。

无论你是想制作这些机器中的一个自己的副本，还是仅仅从它们的创造者的一些想法中获得灵感，这些机器都是实物证明，仅仅因为你现在可以在易贝订购一台便宜的 3D 打印机，并不意味着你必须在 T2 订购。

## 吹笛者 1

由 Alex Balako 设计的 [Piper 1 是自我复制打印机](https://piper3dprinters.com)的一个极好的例子。这种 Prusa i3 风格的设计将标准的 1/2 英寸 EMT 电气导管用于所有结构组件，并带有印刷零件以将所有部件连接在一起。

使用 EMT 导管优于铝挤压导管的优势显而易见:导管便宜得离谱，易于使用，在任何大型五金店都可以买到。大约 6 美元，家得宝将卖给你足够的 1/2 EMT，以建立 200x300x200mm 毫米的 Piper 打印机的变种，并有足够的备用。

这也使得 Piper 非常容易扩展到任意维度。剪下更长的 EMT 长度，换上新的 GT2 腰带，你就可以做生意了。亚历克斯有一个 500mmᶟ变种的可用计划，但对缩放 Piper 的限制更多的是物流(即，你要把东西放在哪里)而不是机械。

如果这种结构对黑客读者来说很熟悉，那可能是因为 Piper 受到了奇妙的[大部分是印刷数控(MPCNC)项目](https://hackaday.com/2016/06/30/a-hydra-of-a-3d-printer/)的启发。就像 MPCNC 一样，Piper 使用一组 608 个“Y”形滑板轴承来骑在 EMT 上，而不是你在更传统的 3D 打印机上预期的线性轴承。

也就是说，这个设计并不是没有问题。Alex 发现，由于打印方向的原因，一些结构件在最初版本的打印机上出现了故障。这些碎片会在层线上简单地剥落，需要重新设计新版本。像这样快速简单地重复设计的能力是 RepRap 思想的一个标志。

 [![errfdiy_piper3](img/ad887652d7d2a9433b3b58229f42c1a5.png "errfdiy_piper3")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/06/errfdiy_piper3.jpg?ssl=1)  [![errfdiy_piper2](img/402d326e7dbd60d5a71876f81919796a.png "errfdiy_piper2")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/06/errfdiy_piper2.jpg?ssl=1) 

如果你想建造一台大型打印机或者甚至激光切割机，Piper 绝对是一个值得关注的设计。轻数控工作甚至不会是不可能的。

 [https://www.youtube.com/embed/HZq3jNRCkO4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HZq3jNRCkO4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



## 伍德斯托克三角洲

[![](img/f53f0c3877dd1af305f2fab847deb83a.png)](https://hackaday.com/wp-content/uploads/2018/06/errfdiy_woodstock.jpg) 真正证明了开源的力量，[约翰·皮肯斯](https://www.thingiverse.com/thing:2139033)的 Woodstock 很大程度上是基于 Rostock 的设计，但融入了他自己设计或在网上找到的大量改进和变化。他提供了他融入到 Woodstock 中的每个设计的链接，以及他对它所做的修改的简要描述，以便让它与所有其他调整和修改一起播放。让某人恰当地评论他们在软件项目中的变更已经够难的了，这就要归功于约翰对所有事情的恰当记录。

最明显的变化是机器的激光切割胶合板框架，以及延长的垂直杆。约翰说，用激光切割框架会使打印机更精确、更坚固，但说实话，它看起来也更酷。除了一些新设计的盒装惰轮外，加长杆还允许通过简单地将整个组件沿杆向上滑动来更容易地调节皮带张力。

Woodstock 还具有一个经过修改的末端执行器，可以接受 [E3D 的直接驱动泰坦挤出机](https://hackaday.com/2018/01/31/the-engineering-analysis-of-plastic-dissolving-lubricant/)，而不是 Rostock 上使用的鲍登设置。正如你可能期望的那样，许多其他组件都得到了加强，以支持这一额外的重量，从展出的印刷品来看，看起来约翰把一切都平衡得很好。一些 RepRap 纯粹主义者可能会抗议激光切割面板，但总的来说，如果你在生活中需要 DIY delta 打印机，Woodstock 看起来是一个非常有前途的选择。

 [https://www.youtube.com/embed/jT24ClLlQKo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jT24ClLlQKo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



## 便携式 3D 打印机

[![](img/e50565391c80c0cd412da1a5ba11bf40.png)](https://hackaday.com/wp-content/uploads/2018/06/errfdiy_bergen1.jpg) 诚然，并不是每个人*都需要*一台可以折叠成手提箱的 3D 打印机，但我们敢打赌，任何人看到约翰·戴蒙德的这一神奇工程壮举都会*想要*一台。被称为“T7”的卑尔根 Makerspace 可运输 3D 打印机在展开和运行时看起来就像一台足够普通的 i3 风格的机器；这很正常，事实上你可能不会多看一眼。但是只要转动几个拇指螺丝，这台机器就可以折叠起来打包运输，几乎只需几秒钟。

没有一个单一的设计元素允许这种快速的转变。卑尔根 Makerspace 打印机的多个细节协同工作，首先是机器触摸屏控制面板上的一个名为“打包”的选项。这命令打印机将挤出机移动到特定的位置，以便当打印机的垂直部分向前折叠时，它不会与任何东西碰撞。

John 对铰链设计感到特别自豪，当用户将打印机的顶部向前折叠时，它会向后移动。这允许打印机的顶部和底部安装在相同的占地面积内，而不牺牲 Z 高度。顶部向下折叠并锁定在底部，集成手柄允许提起机器并将其放入 Hofbauer Megabag 3000 便携包中。甚至还有带子和支架来固定额外的灯丝、电源和一袋工具。

 [![errfdiy_bergen4](img/1eafdf02f7f0f0eac07c7d8839757b01.png "errfdiy_bergen4")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/06/errfdiy_bergen4.jpg?ssl=1)  [![errfdiy_bergen2](img/f54641c49133f2e60b925352ea5d1edd.png "errfdiy_bergen2")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/06/errfdiy_bergen2.jpg?ssl=1)  [![errfdiy_bergen3](img/1c3276b52896fe48fc90c21c1bb9cd47.png "errfdiy_bergen3")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/06/errfdiy_bergen3.jpg?ssl=1) 

在打包去 ERRF 的行李时，John 提到打印机从他的车后掉到了街上，引起了短暂的恐慌。但除了外壳上的一些划痕，你永远不会知道打印机刚刚经历了短暂的跌落和快速停止。一旦展开，它就愉快地印着，好像什么也没发生过。

 [https://www.youtube.com/embed/uWT5Vk2MeXI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/uWT5Vk2MeXI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



## 热情的少数派

我们不会粉饰它:在东海岸的 RepRap 节上展出的真正的 RepRap 打印机少之又少。当你现在可以在亚马逊上花 200 美元买一台 [delta 打印机的时候，建造像伍德斯托克这样的东西看起来很荒谬。但是在 Hackaday，我们是一些人为了确保某件事情完全按照他们想要的方式*进行而不择手段的狂热粉丝。*](https://hackaday.com/2017/08/21/monoprice-mini-delta-review/)

我们向那些自豪的少数人致敬，他们仍在为正义而战，并按照自己的个人规格制造 3D 打印机。[即使花的时间更长，花费更多](https://hackaday.com/2016/07/06/build-a-3d-printer-workhorse/)；最终，你会自豪地拥有一台独一无二的机器，而不仅仅是另一种商业产品。