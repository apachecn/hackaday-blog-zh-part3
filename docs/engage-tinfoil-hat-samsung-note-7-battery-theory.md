# 接合锡纸帽:三星 Note 7 电池理论

> 原文：<https://hackaday.com/2016/10/24/engage-tinfoil-hat-samsung-note-7-battery-theory/>

在很大程度上，我相信事情就像它们看起来的那样。但是每隔一段时间，我开始从一个不同的角度看待值得注意的技术事件。如果事情不像看上去的那样呢？这是阴谋论的领域，我想非常明确地说明这一点:接下来的内容完全是虚构的，不是基于事实。至少，我没有试图把它建立在当前事件的事实基础上。但是也许你可以。如果三星 Galaxy Note 7 手机的电池起火不止这些，会怎么样？

我有一个合理的理论，你愿意戴上你的锡纸帽子跟我一起下这个兔子洞吗？

![Bill Hammack's explanation of uranium enrichment centrifuges](img/b17748814517a11346aa19b3e9468620.png)

Bill Hammack’s explanation of uranium enrichment centrifuges

还记得[震网](https://en.wikipedia.org/wiki/Stuxnet)吗？这是一种计算机病毒，它感染并摧毁了伊朗用于铀浓缩项目的离心机。这些离心机超级精确。它们需要被用来将同位素分离成贫化铀和浓缩铀。这个过程包括不断调整离心机平衡的软件——比尔·哈马克很好地解释了这一点[——破坏这种平衡会损坏设备本身。许多人认为，震网病毒被用于政府支持的对伊朗计划的攻击，以使这些离心机离线。](https://www.youtube.com/watch?v=OcgKDSwINOA)

为什么我现在提起震网病毒？我开始思考三星电池起火事件及其对世界造成的可怕影响。这无疑将三星置于一个艰难的境地——也许是最受尊敬和信任的安卓手机制造商两次弄错了这款手机的电池技术。怎么可能呢？也许是商业间谍。但这当然不是——如果有什么不同的话，你只能称之为企业破坏。

### 你怎么能破坏电池呢？

锂电池内置有监控电路。它们负责在电池变得太平(这会损坏电池)之前切断电池，并在充电期间保持可接受的温度和恒定的电流分布。在某些情况下，它们甚至可以绕过电池，但这更像是电动汽车等应用的一种工业技巧。

 [![Connector has 3 conductors. One is for data.](img/6ad1b604f80e2bc6288641572f2d60f4.png "nexus-5-battery-connector-detail")](https://hackaday.com/2016/10/24/engage-tinfoil-hat-samsung-note-7-battery-theory/nexus-5-battery-connector-detail/) Connector has 3 conductors. One is for data. [![Nexus 5 Battery](img/e0091596fd70946f4ba9f0895ba0a30c.png "nexus-5-battery-connector")](https://hackaday.com/2016/10/24/engage-tinfoil-hat-samsung-note-7-battery-theory/nexus-5-battery-connector/) Nexus 5 Battery

当然，这些电池维护电路运行软件。就在上个月，我们看到了笔记本电脑电池控制器的所有秘密。智能手机通常只有一个电池，但那里仍然有数据——第三个导体可以将温度等数据从电池传输到手机。

如果一个精心制作的病毒能够重写精心瞄准的手机的电池充电代码，并导致它故意失败，会怎么样？由于有如此多的这种特殊模型在野外存在，一个病毒可以被编程为在 99.99%的时间里删除自己以避免被检测到。其余的 0.01%会发挥作用——将细胞的温度推过临界点，从而在燃烧过程中销毁证据。这相当于大约 100 起事故，非常接近被报告的[112](https://www.cnet.com/news/why-is-samsung-galaxy-note-7-exploding-overheating/)。

这是一个令人惊讶的诱人的“假设”，这个思考过程甚至让我想到了其他可能的工业破坏场景。例如，丰田不受控制的加速。但最简单的答案往往是正确的:这些是工程故障。丰田的代码很乱，而且…三星到底发生了什么？他们有生产使用高能量密度锂离子电池的安全手机的记录。我能理解他们有一次弄错了…一次意外。但是当风险如此之高时，他们怎么会犯两次错误呢？

扣除三星股票价值的损失，放弃 Note 7 估计会损失 95 亿美元(是的，10 亿美元)的利润——50 亿美元。这意味着他们本可以为每部手机投入 2000 美元*来解决这个问题，但仍然收支平衡。他们到底是怎么把召回搞错的？投机容易；在电池化学方面飞得太靠近太阳，充电软件中的一个错误，一个尚未被发现的制造过程故障，随你挑。这是一种邪恶的烧电池病毒的几率非常小，但我们已经走了这么远，所以让我们来看看为什么不太可能的原因。*

### 这完全是一派胡言

[![samsung-galaxy-note-7-battery-return-box-instructions](img/8a33fc08aa8efbd49c0853f7ee604bf0.png)](https://hackaday.com/wp-content/uploads/2016/10/samsung-galaxy-note-7-battery-return-box-instructions.png) 

寄回电池的包装说明。你不能编造这些东西。[via[XDA-开发者门户](http://www.xda-developers.com/samsung-sent-us-a-note-7-return-kit-with-a-thermally-insulated-box-and-safety-gloves/)

即使手机电池有可重写的固件或者手机的充电代码可以被攻击，在未经修改的操作系统上从用户空间获取该功能也是非常困难的——而且还有很多人在下载充满恶意软件的 Pokemon Go 版本。

即使有人发现了这样做的方法，难道他们不会通过向三星出售漏洞信息来寻求个人利益吗？三星是修复漏洞的最大受益者。我觉得一个递归阴谋论循环即将到来，所以让我们继续前进。

动机。有人针对三星的动机很少。是的，苹果和三星之间关于手机的公开争论正在由美国最高法院审理。如果你要列出一份可能的破坏嫌疑人名单，苹果会在上面。但是这种想法并没有触及表面。对三星来说，唯一的收获是失去市场份额，对苹果这样的公司来说，风险是巨大的。这一事件可能会玷污电池供电设备的整体市场，损害苹果自己的业务。如果阴谋被发现，后果将是毁灭性的。

有人喜欢看世界燃烧…会不会是独狼黑客？同样，不太可能。这不是勒索软件或[增加你的朋友列表](http://hackaday.com/2016/03/09/the-dark-arts-sql-injection-and-secure-passwords/)。这些故障可能会造成伤亡——任何恶意使用它们的人都会寻求发表声明，而不是在雷达下飞行。

不，这只是一个科幻小说的有前途的情节。具有讽刺意味的是，如果这种回忆(不包括阴谋论)出现在小说中，而不是真实地发生在我们身边，我们都会说这太牵强，难以置信。不要想那些精神控制信号，让我们知道你是否有最喜欢的与技术相关的阴谋论，这太好了，以至于不能留给自己。