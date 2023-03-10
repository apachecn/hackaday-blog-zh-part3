# 回顾:NEJE DK-8-KZ 激光雕刻机

> 原文：<https://hackaday.com/2018/03/01/review-neje-dk-8-kz-laser-engraver/>

当我得到我的第一台 3D 打印机时，我很兴奋，但现在我正考虑在我的收藏中增加一台，我不得不接受这样一个事实，即这些机器在这一点上具有螺丝刀的所有新颖性。这很好。降低成本和提高可用性是将一项利基技术转化为主流工具的关键，就我而言，越多的人在家里或他们的工作室里拥有 3D 打印机越好。但是，探索前沿仍然有一定的刺激，我最近一直在寻找一些新的东西让自己兴奋起来。

[![](img/9a260a22df603919a22ce6b58a422232.png)](https://hackaday.com/wp-content/uploads/2018/02/neje_full1.jpg)

NEJE DK-8-KZ

在我寻求完全的内部制造能力的过程中，激光似乎是一个有趣的下一步，所以我开始研究廉价的设置来尝试一下。在寻找二极管驱动的激光切割机的过程中，我遇到了 NEJE DK-8-KZ。只有 1W，毫无疑问，这款设备不会削减很多。事实上，它是专门作为*雕刻师*出售的。但是考虑到你可以用大约 70 美元的运费买到一个这样的小东西，很难抱怨。

现在我不是 100%确定我会用激光雕刻机做什么，但我认为在投入大量资金(和时间)到更强大的东西之前，这是一个试水的好方法。另外，如果我完全诚实的话，我想从能量谱的低端开始，因为我害怕弄瞎自己。

那么你花 70 美元买了什么样的激光？让我们来看看……

## 五金器具

DK-8-KZ 由黑色激光切割丙烯酸树脂制成，用不锈钢带帽螺钉固定在一起，看起来像是由一套工具制成的东西，但具有足够好的贴合性和光洁度，让人感觉不便宜。这并不是说它可以被称为任何想象力的延伸，因为它站在不到 8 英寸高。一方面，这意味着当你不使用它时，可以方便地扔在架子上，但 DK-8-KZ 的小尺寸实际上是它的工作区域非常小，大约为 40 毫米 x 40 毫米

DK-8-KZ 被限制在如此小而特定的运动范围内有一个很好的原因:该设备的 X 轴和 Y 轴都依赖于从光驱中重用的硬件。我得到的印象是，在中国发现了一个仓库，里面装满了基本上过时的光驱，有人想出了一个绝妙的主意，用它们精确的运动作为一系列微型激光雕刻机的基础。(编者注:我们试图在 Hackaday 上找到这种设备最早的出现，想出了[这个机器](https://hackaday.com/2010/08/26/building-a-laser-cutter-from-a-weak-laser/)。看看能不能找到更老的！)

 [![neje_laser](img/77daae3ea5507908c8590595f5adf67d.png "neje_laser")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/02/neje_laser.jpg?ssl=1)  [![neje_laser2](img/8acb98a7cf21ee6749d242922a6adfbc.png "neje_laser2")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/02/neje_laser2.jpg?ssl=1)  [![neje_ribbon](img/8afa0f3dae8fcdef7ba555c56ba1b0f8.png "neje_ribbon")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/02/neje_ribbon.jpg?ssl=1) 

## 软件

NEJE DK-8-KZ 确实有一张光盘，里面有该设备的驱动程序和软件，但我很快就把它扔进了垃圾桶。首先，我不会相信这款设备的内置软件。但更实际地说，我已经没有 Windows 电脑了，所以它不会给我带来任何好处。幸运的是，NEJE DK-8-KZ 有一个相对简单的控制协议，有几个项目可以让它运行起来。

就我个人而言，[我一直在使用 EZGraver](https://github.com/camrein/EzGraver) 并且运气非常好。它是开源的，可以在 Linux、Windows 和 OSX 上运行。如果你不想使用 Qt 前端，它甚至有一个命令行界面。

EZGraver 的工作流程非常简单。连接到硬件后，加载 512 x 512 的黑白图像，并根据需要调整缩放和旋转控件。还有一个设置，你希望激光燃烧多长时间，这在处理不同的材料时变得很重要。一旦预览看起来不错，你的刻录时间设置，你上传工作到 NEJE DK-8-KZ，并点击“开始”。

我发现 NEJE DK-8-KZ 的一个有趣之处是，计算机并不直接控制它。图像和选定的设置被上传到机器上，然后你可以断开电脑连接，通过点击机器顶部的红色按钮开始刻录来无线使用它。

## 烦恼

我不想把 NEJE DK-8-KZ 打得太惨，因为它非常便宜，而且你可以假设，当你购买由 DVD 驱动器外壳制成的产品时，这种体验不会是完美的。但是如果你决定沿着这条路走下去，还是有一些事情需要提及。

[![](img/8ba301ee098f1e598c1a27be6e6f4511.png)](https://hackaday.com/wp-content/uploads/2018/02/neje_drift.jpg)

Dots indicating where the focal point was while focusing

首先，给它供电。设备侧面有一个 5 V 电源桶型电源连接器，为此需要自备交流适配器。但是，即使你已经连接，板需要通过 USB 连接自己的 5 V。长话短说，即使你没有使用 NEJE DK-8-KZ 连接到你的电脑，你需要有两个端口供电。这对于普通的 5 V USB 电源适配器来说没什么大不了的(我有一整箱这样的适配器)，但是看起来很草率。

也许我发现的 NEJE DK-8-KZ 最大的问题是光学质量。你需要手动将激光聚焦到你正在加工的物体上，因为焦点需要尽可能的紧密以获得良好的燃烧。唯一的问题是，当你转动聚焦镜头时，它会到处乱舞。没有办法在焦点不漂移的情况下将激光聚焦，这意味着像暂停刻录来调整焦点这样简单的事情实际上变得不可能。

最后，虽然这没什么大不了的，但我不得不提到他们是如何处理激光制导的。没有你可能会想到的终点停止开关，相反，固件只是简单地运行电机向后 20 秒左右；每次打开它都会发出可怕的摩擦声。

## 实际结果

当然，像这样的东西真正的问题是它实际上燃烧得有多好。事实证明，相当不错。我烧过纸、纸板、木头和塑料，结果都很好。它可以很容易地切割纸张和 3M 油漆工的胶带，这在制作绘画和蚀刻的模板方面具有一些有趣的可能性。

 [![neje_wood](img/ff7d3af443c2f7ad87ba371f5aa4c18f.png "neje_wood")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/02/neje_wood.jpg?ssl=1)  [![neje_plastic](img/ffa6b2a66c070bfc9e65f317c647fbdd.png "neje_plastic")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/02/neje_plastic.jpg?ssl=1)  [![neje_cardboard](img/bfe86d023c9ea10d433e7635a475ec36.png "neje_cardboard")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/02/neje_cardboard.jpg?ssl=1) 

## 但是关于……

[![](img/f9a6b5939a717f24e0fe986136509a96.png)](https://hackaday.com/wp-content/uploads/2018/02/neje_magnified.jpg)

Magnified 250X

如果你正在阅读 Hackaday，你可能想知道你是否可以使用 NEJE DK-8-KZ 制造多氯联苯。[过去，我们已经展示过有人使用非常相似的设备](https://hackaday.com/2016/03/14/laser-pcb-exposer-built-from-cd-rom-drives/)处理预敏化的光刻胶印刷电路板，这样应该可以很好地工作。

但是如果你只有一些普通的覆铜板呢？我试着用黑漆喷涂一小片木板，但激光似乎不足以完全烧蚀掉它。我用黑色指甲油的效果更好，但仍然没有找到合适的设置来获得干净的烧伤。当在显微镜下观察时，你可以看到激光没有完全去除指甲油，这阻碍了我蚀刻的尝试。

我还没有放弃。诀窍可能是用激光多次通过，甚至在烧板后用某种研磨剂或刷子擦掉最后一点点指甲油。我计划继续这样做，如果我能从 NEJE DK-8-KZ 得到一些好的主板，我会发布一个更新。

## 最后的想法

NEJE DK-8-KZ 是这样一个老黑客，如果有人把它作为自己的项目发送到 tip line，我们会问自己，如果我们想运行另一个 CD-sled 数控机床。(当然，我们愿意！)这并不是说要打击它——老实说，我对 NEJE 设法处理本质上是电子垃圾的做法印象深刻。把这样一个肮脏的黑客变成一个产品至少值得一提，如果不是一些快乐的扳手。它并不完美，但是一旦你习惯了这种怪癖，结果就不言自明了。

这个东西[远不如其他“廉价”激光](https://hackaday.com/2017/12/22/improving-cheap-laser-engravers-for-pcb-fabrication/)，也无法与[的 K40](https://hackaday.com/tag/k40/) 相提并论。但是对于 70 美元来说，我认为这是一笔非常划算的买卖。它不太可能是你的最后一台激光，但它是你第一台激光的绝佳选择。