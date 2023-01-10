# 当撇油器不是撇油器时

> 原文：<https://hackaday.com/2018/01/02/when-a-skimmer-isnt-a-skimmer/>

我有一件事要坦白:自从我第一次在网上读到它们的时候，我就非常渴望在野外找到一个自动提款机。同样是这种病态的好奇心让我们对车祸视而不见，你不想目睹任何人受伤，但仍然有近距离看到潜在危险的欲望。虽然我承认我的兴趣很大程度上是自私的(我已经知道我会在哪个架子上展示它)，但如果有一个 ATM 机防盗器经过我的道路，仍然会给社区带来实实在在的好处。显然，我会将它从机器中移除，防止其他人成为它的猎物，[而不可避免的拆卸将为 Hackaday](https://hackaday.com/2016/05/03/reverse-engineering-an-atm-card-skimmer/) 的好读者提供有趣的内容。这对每个人来说都是一个胜利，当然在这个探索中命运应该站在我这边。

因此，当我去当地的 ATM 机插入我的卡时，当我的手指碰到 3D 打印塑料那种明显的粗糙感时，我的心脏漏跳了一拍。这么多年后，我的梦想实现了。任何人都不应该因为可能成为欺诈的受害者而如此兴奋，但我就在那里，在农贸市场像个白痴一样咧着嘴笑。像任何一个猎人一样，我迅速给我的猎物拍了一张照片，留给后代，然后试图把它从主机中释放出来。

但是事情并没有像预期的那样发展。我大部分空闲时间都在为 Hackaday 写博客，所以可以肯定地说，体力并不是我所拥有的大量属性，但即使如此，我无法让 skimmer 脱离似乎还是很奇怪。我朝各个方向猛拉它，试图旋转它，做了除了踢它以外的所有事情；但是绝对没有动静。事实上，我注意到，当拉动撇渣器时，自动取款机的整个面板都凸出了一点。我意识到这东西不仅仅是粘在机器上，它一定是被安装在机器里面了。

丢下我的奖品让我心碎，但至少我可以提醒负责的一方。提款机上写着提款机主人的联系方式，所以我用电子邮件把照片和所有相关信息发给他们，希望他们能在有人被骗之前来检查提款机。

## 出乎意料的反应

到家的时候，我的收件箱里收到了自动取款机老板的回复。但与其说是为造成的不便道歉，并发誓要调查此事，不如说是一条信息，告诉我我遇到的根本不是一个骗子。这是他们自己设计的 3D 打印读卡器，取代了原来的硬件。邮件接着说，这种定制读卡器背后的想法是，它实际上可以*防止*安装套卡机，因为这是意想不到的。

成功安装撇油器的一个关键因素是调查您想要锁定的 ATM，在本例中是 Nautilus Hyosung 1800 SE。一旦攻击者知道他们正在对付的是哪台机器，他们就可以在网上为它购买一个替换的读卡器，并且知道当他们去安装它时，他们设计的任何适合它的设备都将在“活动”的机器上工作。对于其中的一些机器，如果你知道去哪里找的话，读卡器的 3D 模型已经可以在网上找到了。

但是想象一下，你戴着滑雪面罩，手里拿着提款机出现在自动取款机前，却发现这款晓星的读卡器和你研究的完全不同。取而代之的是，阅读器看起来像是来自杜宝 R&D 实验室，让你所有的精心策划变得毫无价值。又一个被几何学挫败的罪犯。

我认为这个想法很吸引人，这当然是我第一次听说。我回答说，问他们是否愿意在网站上讨论一篇文章的想法，但他们希望保持匿名。确定 ATM 机所有者或他们操作的地理位置会危及他们修改的重点，所以我可以理解他们不愿意记录在案。但是我们还是可以看看这个想法本身。

## 针对持续威胁的动态防御

渗出解放军是我的精神动物，所以我的脑海里立即出现了使用 3D 打印技术为自动取款机生产“键控”读卡器的想法。像这台机器的所有者一样创建一个自定义阅读器是一个很好的第一步，但它仍然是一个静态设计，最终可以被考虑。如果不是为你所有的自动取款机打印出完全相同的读卡器，而是让每一个都是独一无二的，几乎让人无法预料，那会怎样？

这项技术很容易想象。借助 OpenSCAD 等参数化 CAD 工具，核心读卡器设计的表面可以基于随机种子进行扩展。小的几何突起可以通过程序生成，并为每台机器打印一个新的阅读器。在撇油器更常见的高价值市场，新的阅读器甚至可以定期生成和打印。

作为一个简化的例子，我编写了一个快速的 OpenSCAD 脚本，它将读卡器表面的几个“针”的数量和垂直高度随机化。每次生成新的 STL 进行打印时，管脚的布局都会不同。这种不可预测的表面将使其更难与撇油器紧密贴合，从而更难隐藏。

 [![skimmer_demo3](img/fcf6f03acfe5ab16196ddae694ea0f31.png "skimmer_demo3")](https://i0.wp.com/hackaday.com/wp-content/uploads/2017/12/skimmer_demo3.jpg?ssl=1)  [![skimmer_demo2](img/d2830a2ec069fb230cfa0cb5aaefd0b3.png "skimmer_demo2")](https://i0.wp.com/hackaday.com/wp-content/uploads/2017/12/skimmer_demo2.jpg?ssl=1)  [![skimmer_demo1](img/5bcf7ff5df3a42e316f296821ef3165b.png "skimmer_demo1")](https://i0.wp.com/hackaday.com/wp-content/uploads/2017/12/skimmer_demo1.jpg?ssl=1) 

这个脚本的完全实现版本可以对读者做出更剧烈的改变，每次生成 STL 时从根本上改变它的几何形状；使得适应几乎不可能。想象一下，一个小偷来安装他们的撇油器，却发现自从上次他们在那里之后，阅读器已经变成了椭圆形。

## 不可行的解决办法

用 3D 打印部件(动态生成或其他方式)迷惑 ATM 机的读卡器，听起来是一种相对廉价和简单的迷惑窃贼的方法，但这种想法有一个巨大的问题。如果你告诉消费者要时刻警惕连接在自动取款机上的可疑硬件，那么在自动取款机上安装*你自己的*可疑硬件作为威慑没有多大意义。

我很欣赏这台自动提款机的主人的想法，至少他们在尝试跳出框框思考。但我内心的现实主义者不禁认为，这一切只会导致联系他们的人越来越多，因为他们的自动取款机看起来很奇怪。哄骗消费者对安装在自动取款机上的奇怪部件产生虚假的安全感并不是一个可行的解决方案。虽然最近在远程检测撇油器方面做了一些有希望的工作，但这个问题仍然需要有人来解决。

有什么想法吗？