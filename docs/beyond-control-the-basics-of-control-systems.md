# 超越控制:控制系统基础

> 原文：<https://hackaday.com/2015/12/02/beyond-control-the-basics-of-control-systems/>

控制系统正是你所认为的那样:设计用来控制某些东西的系统。或许更好的说法是系统设计控制某些东西的行为。“控制系统”这个术语非常模糊，我们大多数人(最初)都不会过多考虑它，直到它引起我们的注意，或者我们让一个机器人电枢撞向它本身，并调查那个可怕的事件是如何发生的。通常在调查过程中，我们的内部对话会有一个类似这样的循环:“为什么系统会允许我以自我毁灭的方式操纵它！？!"

我发现是我自己的无知，我没有实施一个适当的控制系统。有人可以声称我没有考虑任何控制系统。我跳得太深，太快(听起来熟悉吗？)并付出了旋转臂撞向系统另一部分的代价。幸运的是，一位朋友介入并为我修复了手臂，并隐喻性地指着墙上的一个大型霓虹灯招牌说:“你不能忽视这个”。他走过去拉了拉悬挂在标志下的链子，高压给管子里的气体充了电，让我看不清现在不可避免的明显的词:**控制系统**。

## 控制系统的证据

![Ancient-Egyptian-Water-Clock](img/c1e347d021e9f0be55161b091d0d399b.png)

Source: [Globe Rove](http://globerove.com/egypt/ancient-egyptian-water-clock/3235)

有证据表明控制系统就在我们周围，我们整天都在使用它们，却没有给它们任何思考。我在半夜迷迷糊糊地起床，像个僵尸一样拖着脚步走过走廊去喝水，我伸出的胳膊从未错过橱柜的把手。我毫无问题地将橱柜的门打开适当的距离，用另一只手抓住一个玻璃杯。我做这些事情的时候并没有积极地关注它们，但是，这些都是控制系统。当我从橱柜中拿起杯子时，我没有挤压它，直到它在我手中粉碎。我也有能力打开水龙头的水，注满玻璃杯，关掉水，唯一湿的是玻璃杯的内部，而不是我的手甚至是水龙头下面的洗手盆。这是许多复杂控制系统致力于一杯水的一个例子。

火箭点燃并推动卫星进入地球轨道，电梯把我们送到期望的楼层，控制系统无处不在。它们一直存在，可以在我们的一些 STEM 祖先(我想我刚刚创造了这个词)最著名的作品中看到。

公元前 300 年，希腊数学家和发明家 Ktesibios 发明了一种水钟，它使用一种控制系统，以水作为输入，以时间作为输出。水和时间之间的一切都是控制系统。

1809 年，威廉·库比特改进了以前的风车设计，制造了带自动百叶窗的风车帆，百叶窗可以根据风速和配重进行调节，这是一个控制系统。风是输入，恒定的旋转能量是输出。

![Source: http://www.shipleywindmill.org.uk/mill.htm](img/02a48f8540850b9c8cccf4061b0f3604.png)

Source: [Shipley Windmill](http://www.shipleywindmill.org.uk/mill.htm)

观察一个现有的系统，指着输入和输出说“进水，超时，它们之间的一切都是一个控制系统”并不能解释控制系统是如何工作或设计的，但我们正在接近这一点。这些发明需要一些相当复杂的数学，我们将在后续文章中讨论，但现在我们正在为理解打下基础。我们已经看了一些自然控制系统和一些人造控制系统的例子。我分享了我对控制系统的无知，然后试图通过告诉你我可以装满一杯水来挽回自己。

我们还会看一些框图，我应该提醒你，在某些时候，我们会遇到一些你再也不想看到的数学。幸运的是，当我们看到这些可怕的数学时，我们要做的第一件事就是制定一个计划离开那里。一旦我们安全脱离危险，我们将处理一些简单的操作，也就是说，我们将做一点代数，而不是微积分和微分方程。现在跟我来，朋友，休息过后，真正的乐趣开始了。

## 框图

为了我们的目的，我已经草拟了一个单输入单输出(SISO)控制系统的简化版本。框图中的 ***是*** 控制系统。我们可以用代数来操纵它，并根据需要引入新的组件来获得期望的输出。然而，我们将很快用更好地描述系统元素的标签替换这些通用标签。我们还将把“控制系统”模块分成多个模块，组成系统。你可以把这个图想象成你给孩子的高级描述，记住“进水，超时，它们之间的一切都是一个控制系统”。接下来的一点更详细，但仍然是象征性的，因为我们还没有看到每个模块的数学组成部分。

![black_basic_sinlge_block](img/9a37f4d2845fb807cc67181fe212a836.png)

让我们创建一个我们假设要设计的特定控制系统的例子。大型卫星天线怎么样？很好，完成了。所以我们有一个由齿轮马达驱动的大型卫星天线。使用电位计输入碟形天线的期望位置，控制器使用该电位计来确定实现期望输出所需移动的幅度和方向。此外，还要考虑电机本身、我们要移动的负载(大型卫星天线)以及这样做所需的传动装置。这个系统的输出要通过一个叫(等一下)，反馈的东西反馈到输入。反馈路径包含第二个电位计，该电位计随着碟形天线的旋转而调整，并进入与输入的求和点。

我们现在可以画一张新的框图来更详细地描述我们在这个系统中所进行的工作。

![Untitled 2](img/2731230bf3e66e4e5e98321681b949d0.png)

我们已经讨论了系统的功能块和基本流程，让我们看看信号，在上图中用蓝色表示。初始角度输入是电位器(输入传感器)转换成电压的角度。在求和点有两个信号输入和一个输出，两个输入是与输入成比例的电压和与输出成比例的电压。如果您注意到输入信号上的极性标记，我们有输入减去输出，这产生了错误信号。角度输出实际上是与碟形天线指向的方向相对应的角度。为了在我们的控制系统中使用该角度，右边的电位计(输出传感器)将该角度转换为发送至求和点的电压。该连接点负责比较用户控件，并确保在实际位置与之匹配之前采取行动。

## 修改系统

如果我们知道系统的行为是将误差信号驱动为零，那么我们有两种方法来测量系统的输出。**瞬态响应**和**稳态误差**都可以测量，以分析我们的控制系统的结果，并相应地修改它。

![](img/021c0b92267099078edb62e2d257c181.png)

瞬态响应是信号对系统变化的反应，可以在右侧的阶跃响应图中看到。根据使用的阻尼比类型，有 3 种类型的瞬态:过阻尼、欠阻尼和临界阻尼。目标是使响应尽可能接近临界阻尼。

如果我们将曲线响应视为一部从地下室到一楼的电梯，就可以想象出瞬态和稳态误差的重要性。阻尼不足的振动显然会成为一个问题，并可能导致一些不安的胃在前进的道路上，作为超速电梯过了地板，并在相反的方向过度补偿，反复。过度阻尼的电梯最终会以非常平稳的方式把我们带到那里。临界阻尼响应以红色显示，定义为无振荡的最快建立信号。

关于我撞毁的机械臂，我想知道为什么会这样，我们可以在阶跃响应图中看到这个问题的答案。可能我正在控制一个欠阻尼系统，手臂在振荡的前半个周期过冲时崩溃，如图中的蓝线所示。

[![sat_sim](img/0a48a61f540c1fdd498c8bbde98cc68f.png)](http://www.wiley.com/college/nise/0471794759/swf/AntenaChap1.swf)

Interactive Antenna Simulation (gain control)

在这个例子中，没有引入任何稳态误差。电梯场景中的稳态误差将导致电梯门在楼层 1 和楼层 2 之间的某处打开。如果是这种情况，我们将通过改变我们的控制器来处理稳态误差，使得门在 1 层打开。

单击左侧的天线模拟屏幕截图将带您进入新选项卡中的交互式模拟器(需要 flash)。您可以摆弄增益值，看看它如何改变输出响应。提示:你必须点击倒带按钮开始一个新的模拟。

## 转移函数

传递函数在概念上类似于系统的增益，定义为输出与输入之比。对于控制系统，我们使用传递函数这一术语而不是增益，因为它意味着使用 s 域(我意识到我还没有介绍“s 域”到底是什么，但我们暂时忽略这一点，因为它将在另一篇文章中解释)来获得系统的期望响应。

我们画的框图包含了很多关于控制系统的信息，主要是缺少系统建模所需的数学知识。传递函数是数学可以找到的地方，在我们的系统中是控制器(数学)和设备(更多数学)的组合。

### 控制器和设备

控制器包含驱动大型电机的信号和功率放大器的数学模型。该工厂包含代表我们的电机规格的数学模型，这些模型在现实世界中很容易获得，包括电机在特定电压下的 RPM 和电机电阻等内容。我们还需要关于马达和卫星之间的齿轮比的信息(这是一个机械放大器)。电机在运行期间会有一个机械负载，我们可以用一个等效的机械负载方程来预测这个负载，该方程使用:负载的等效粘性阻尼和等效负载惯性。为了与本介绍的无数学主题保持一致，我们将暂时跳过这在数学上意味着什么。

## 最后的想法

本文的目的是阐明什么是控制系统以及它们如何工作的基本概念。我认为控制系统是有趣和令人兴奋的，因为我们可以计算一些在复杂系统中使用的变量，而不是对非平凡的未知进行胡乱猜测(这曾经是我的难题)。

作为黑客和工程师，我们像其他人一样学习曲线，就像其他人一样，我们有时会在改进自己设计的能力上达到一个平台。我认为对控制系统的基本理解可以帮助我们很多人度过这次衰退。我会像我的朋友帮助我一样帮助你，让我了解什么是控制系统，如何分析系统中正在发生的事情，我们都会在设计自己的系统的过程中变得更好。

## 下次会发生什么

在下一期的《超越控制》中，我们将看一些电力系统在时域中的例子。我们将讨论它们在 s 域中的传递函数，为什么我们需要 s 域，以及从时域到 s 域(以及返回)需要什么。那是我说数学的两句话，没有说数学。下次见！