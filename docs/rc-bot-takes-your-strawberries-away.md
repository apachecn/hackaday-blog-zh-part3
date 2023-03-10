# 遥控机器人把你的草莓拿走了

> 原文：<https://hackaday.com/2016/07/10/rc-bot-takes-your-strawberries-away/>

不要让这辆遥控推车上友好的微笑欺骗了你，它会把你的草莓带走——尽管这是重点。这是一辆遥控汽车，[晶体管人]和几个朋友改装的[，用来在草莓地里运送刚摘下的草莓](http://transistor-man.com/adventures_of_strawberrybot.html)，这样你就不用。

![RC strawberry carrying robot before putting on the cooler](img/b401fee9533db8b988bd96eeb0c749d6.png)

RC strawberry carrying robot – WIP

他们从一辆较旧的 Traxxas Emaxx 开始，这是一辆 4 轮驱动的 RC 怪物卡车。该团队还在当地五金店买了一个合适大小的水冷却器。快速负载测试表明，5 磅的重量使弹簧和减震器塌陷，导致底盘接近地面下沉。研究小组有两个选择:换上更坚固的弹簧或者完全不使用弹簧。他们决定用金属板代替一组电击，有效地锁住它们。之后，是时候进行一些 CAD 工作了，接着是使用喷水器切割一些铝板。他们很快就有了一个饮水机安装板。这个安装板被固定在 4 根柱子上，这 4 根柱子最初是用来固定车辆的 Lexan 车身的。缠绕在冷却器和安装板上的柱上的松紧绳将冷却器保持在适当的位置。

![Thermal image of bad MOSFET](img/1574c60f8e15c67509aaac58d401e298.png)

Thermal image of bad MOSFET

一些初步测试表明，即使在低速档，车辆也移动得太快，容易翻倒，正如你在下面的第一个视频中看到的。一些实践有所帮助，但 3:1 减速行星变速箱使车辆降至步行速度，产生了很大的差异。我们安排了一次去当地红火场草莓采摘场的旅行，但首先还是有些兴奋。凌晨 1 点，UNIK 320A 高压速度控制器冒出一些神奇的烟雾。用热感相机快速检查发现了罪魁祸首，其中一个 MOSFETss 失效了，在用一个足够接近的 MOSFET 替换它后，它们又重新开始工作了。

正如你在下面的第二个视频中看到的，在草莓地里的测试进行得非常顺利，尽管不是没有一些小费。孩子们也发现这是摘草莓的一种有趣的消遣，在假装的恐惧和喜悦之间交替。

他们还考虑了一些增强措施，例如增加一个加速度计来控制速度并减少倾斜。还研究了实现“跟我学”行为的方法。该团队还研究了使用帕尔贴冷却器来冷藏草莓。珀尔帖效应需要很长的冷却时间，而冰袋却能很好地完成这项工作。

下面是一些测试，虽然仍然有点 tippy。

[https://player.vimeo.com/video/172301100](https://player.vimeo.com/video/172301100)

这里你可以看到他们在草莓农场测试。

[https://player.vimeo.com/video/171535571](https://player.vimeo.com/video/171535571)

我们能想到的另一个改进是让这个装啤酒的机器人在炎热的采摘草莓的日子里给你送啤酒来降温。即使在冬季也可以采摘，这里有
【迪诺】[室内水培草莓农场](http://hackaday.com/2012/02/08/hydroponic-strawberries-sweeten-up-winter-dolldrums/)，也使用类似冷却器的容器。