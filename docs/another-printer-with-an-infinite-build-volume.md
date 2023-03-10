# 另一台具有无限构建容量的打印机

> 原文：<https://hackaday.com/2017/05/12/another-printer-with-an-infinite-build-volume/>

我们很少看到 3D 打印机不仅仅是当前标准做法的改进。[Prusa]的单轴四色打印机也榜上有名，但它不久前才上市。在去年 200 美元的单价打印机中发现的新颖的 32 位控制器板有可能改变家庭手工业。除了这两个例外，3D 打印的创新真的没有看到我们在 2010 年或 2011 年看到的收益。

[![](img/be10125ab5b2a57454f23dd88b53bc5e.png)](https://hackaday.com/wp-content/uploads/2017/05/2q.jpg) 荷兰的一家公司 Blackbelt 3D，[推出了自去年三月以来我们见过的最具创新性的 3D 打印机](http://blackbelt-3d.com/)。这是一台无限卷 3D 打印机，专为自主生产而打造。这台打印机可以生产一排又一排的 3D 打印零件，或者它可以打印比构建板更长的对象。如果你有足够的时间、灯丝和电力，没有理由你不能打印出数百米长的塑料光束。

这台打印机上的规格大约是你对一台大型工业或原型机器的期望，而不是一台旨在打印拖船和坐立不安的纺纱机的机器。Blackbelt 为 hotend 使用可互换的打印头，配有 0.4、0.6 或 0.8 毫米喷嘴。长丝进料是一个鲍登，挤出机隐藏在控制面板下。框架是显而易见的博世挤压，机器的体积是 340 毫米乘 340 毫米无论如何。(Kickstarter 上的)零售价为 9500€，但额外支付 3000€，你还可以得到一个底部带脚轮的整洁支架。当然，有了无限的构建体积，你也可以*打印*一个支架。

### 但是等等，这个不是有专利吗？

围绕 Blackbelt 3D 打印机的大多数在线评论都集中在 RepRap 项目的一个被遗忘的分支上。RepRap 项目的[连续皮带生产](http://blog.reprap.org/2010/07/continuous-belt-production.html)促成了 MakerBot 自动构建板的开发。不幸的是，MakerBot 的自动构建板的[方法](https://www.google.com/patents/US8287794?dq=inassignee:%22Makerbot+Industries%22&hl=en&sa=X&ei=Ht5nUoTKF87wkQe5mYCYBg&ved=0CFoQ6AEwBQ)和[装置](https://www.google.com/patents/US8282380?dq=inassignee:%22Makerbot+Industries%22&ei=Ht5nUoTKF87wkQe5mYCYBg)很快在 Stratasys 规则下获得了专利，APB 的开源开发陷入停滞。这种发展下滑的原因可能是害怕诉讼，或者是 APB 一开始就没有那么好地发挥作用。

关于黑带的在线评论和追溯到[查理·帕克斯]和 NYC Resistor 的一个项目的开发谱系实际上是不正确的。我们第一次看到这样的事情是在去年三月，在中西部说唱音乐节上。在那里，Polar3D 的[Bill Steele]展示了他过去几个月一直在做的一个项目。根据[Bill]的说法，这是一台无限体积 3D 打印机，被设计成 MakerBot 的一个机械中指。

在 MRRF 展示的无限构建体积 3D 打印机很简单，但构建黑带的所有构件都在那里。床倾斜 45 度，床是一个传送带，只有一点点 g 代码的魔力来把一切都集中在一起。

在与[Bill Steele]交谈时，他说他对商业上追求“无限 3D 打印机”的概念不感兴趣，这种构建只是因为 MakerBot 的一项糟糕的专利才成为可能。例如，MakerBot 的专利将 XYZ 轴与床分离，并要求床是平的。[Bill]的工作绕过了这些专利，并在这个过程中创造了一台无限体积的 3D 打印机。

虽然[比尔]的未命名但非常创新的 3D 打印机只在 MRRF 短暂亮相，但那里的一些人发现它是近年来最具独创性的打印机。显然，Hackaday 的文章也吸引了一些眼球:Blackbelt 3D BV，Blackbelt 打印机背后的公司，在 MRRF 会议后一周成立。

现在，随着概念的验证，我们真的很期待 RepRap 风格的无限构建量 3D 打印机。一台组装体积为 200 毫米乘 200 毫米乘*或者其他什么*的成套机器将会是惊人的。它可以打印出一系列 3D 打印的拖船，或者一些不适合普通打印机制造量的非常有趣的零件。虽然我们无法预测 Blackbelt Kickstarter 的未来——以及 Kickstarter 上 3D 打印机项目历史的标准提醒——但 DIY 无限构建卷打印机将是非常棒的，我们不能等待社区站出来接受挑战。