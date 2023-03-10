# 逻辑噪声:利用 R-2R DAC 实现数模转换

> 原文：<https://hackaday.com/2015/11/05/logic-noise-digital-to-analog-with-an-r-2r-dac/>

用数字逻辑发声通常需要一个数模转换器。建造一个非常简单，R-2R 梯子的音质实际上非常好。

在上一版的《逻辑噪声》中，我们[构建了一个(相对)简单的 VCO](http://hackaday.com/2015/09/11/logic-noise-playing-in-tune-with-an-exponential-vco/)——压控振荡器——其响应大约为每倍频程 1 伏。我甚至演示了它如何与另一个 synth 的键盘协调工作。但是，如果你没有一个控制电压键盘，或者你想要将我们已经构建的所有基于逻辑的电路与其他受电压控制的电路结合起来，该怎么办呢？这就是数模(DAC)电压转换器的用武之地。

 [https://www.youtube.com/embed/kDONGJxYnPw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/kDONGJxYnPw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



## R-2R DAC:分压器一直向下

在本次会议中，我们将组装一个简单的 DAC，以便稍后可以使用逻辑电路输出(模拟)控制电压。过去，当我们需要非逻辑电压时，我们会将电位计连接到两个电压轨，并从中心引脚拉掉中间电压，输出电压会随着旋钮的转动而变化。考虑到这一背景，我们将使用大量电阻来构建能够产生逻辑选择的中间电压值的 DAC，这一点也许不会令人惊讶。

事实上，一个两端连接到`VCC`和`GND`的电位器就是一个[分压器](https://en.wikipedia.org/wiki/Voltage_divider)。但它们比这更普遍——将两个电阻串联起来。现在给它们加上电压。两者中间的电压取决于两个电阻的值，就像 T4 一样。

[![voltage_divider.sch](img/056f3dce1b5195681b3e1724d1edb294.png)](https://hackaday.com/wp-content/uploads/2015/10/voltage_divider-sch.png)

假设你想把一个电压分成两半？将一端接地并设置 R1 = R2 很好地完成了这个任务，并且与你的直觉完全吻合。如果所有的电压都降在两个电阻上，并且它们的值相等，您可能会猜测每个电阻上的电压降了一半。嗯，确实是。

为了构建 DAC，我们希望每个输入位产生特定的输出电压，然后将它们相加。特别是，如果我们希望将电压编码为二进制表示，我们只需确保阶梯的每一级对最终输出的贡献是前一级的一半。

这正是 [R-2R DAC](https://en.wikipedia.org/wiki/Resistor_ladder) 的作用。R-2R 梯形电阻由二分频级组成，因此当你将一个逻辑电压(我们称之为`VCC`和`GND`电平)施加到梯形电阻的最高一级时，你会得到`VCC/2`或`GND`。在梯子上再加一个横档，最上面的横档仍然产生`VCC/2`或`GND`，下面的横档产生`VCC/4`和`GND`。现在梯形可以输出四种可能的值:`GND`、`VCC/4`、`VCC/2`和`3/4*VCC`。

[![r2r_dac.sch](img/7498b1ecb272a3bd17db096a73526263.png)](https://hackaday.com/wp-content/uploads/2015/10/r2r_dac-sch.png)

随着我们向阶梯中添加越来越多的级，我们的最高电压越来越接近`VCC`，并且随着每个新级的出现，最小的电压步长被减半。例如，用两位我们可以表示数字 0、1、2 和 3，最小电压步长是`VCC / 2^2^`，因此产生的最大电压是`3/4*VCC`。八位，最小电压步长为`VCC/256`，最大电压为`255/256*VCC`。

### 泰文等效电路

如果你不满意我对上面电路的挥手式解释，你需要了解一点关于 [Thévenin equivalence](https://en.wikipedia.org/wiki/Th%C3%A9venin%27s_theorem) 的知识，但这并没有那么糟糕。基本逻辑是，任何带电压源的纯阻性电路(就像我们这里得到的一样)都可以视为只有一个电阻和一个电压源。你可以反复这样做，这样我们就可以往上走，把下面的一切都折叠成一个等效的电压源加电阻。

在计算 Thévenin 等效电阻和电压时，假设输入对地短路，然后计算电阻。从第一个结点(电路图中电阻`R1`和`R10`之间)看，我们有两个 100k 的电阻并联，所以第一级的 Thévenin 等效电阻是 50k 欧姆，如果`D0`导通，结点处的电压`V0`是`VCC/2`，如果`GND`关断。

[![thevenin.sch](img/5ae7dab97205fd3005fdc2ee8e41df92.png)](https://hackaday.com/wp-content/uploads/2015/10/thevenin-sch.png)

向上移动阶梯中的下一个梯级，再次使用 Thévenin 技巧，我们看到两个 50k 电阻(实际上是 100k)再次与一个 100k 电阻并联。因此，将`V0`和`D1`视为接地，等效电阻再次为 50k 欧姆。当`D0`关闭时，`V0`为`GND`，输出电压因此根据`D1`为`GND`或`VCC/2`。

另一方面，如果`D0`开启，`V0`就是`VCC/2`。当`D1`关断时产生的等效电压是`VCC/4`，当`D1`接通时是在`VCC`和`VCC/2`或`3/4*VCC`的中间，正如我们上面所说的。继续折叠各级，记下所有可能的电压，你将得到我们之前讨论过的二进制阶梯。QED 'ed。

如果你需要在 YouTube 上看到它才能相信，这里有一个很好的视频解释它是如何工作的。

### 布丁的味道才是最好的证明

最后，如果这些对你来说都不够好，而且你也有我的经验主义倾向，那就从头开始构建你自己的，并用电压表测试每个阶段。或者如果你分享我的经验主义倾向，但你很懒，就看这个视频吧。

 [https://www.youtube.com/embed/MB73ohE-t4w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MB73ohE-t4w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



### 实施细节

原则上，您可以用任意多的步骤构建 R-2R DAC，但最终会遇到器件本身的精度问题。使用高质量的 1%容差电阻时，8 位 DAC 指日可待，但如果不购买更高质量的器件，更进一步就没什么意义了。为了产生类似的波形，你可以用更少的步骤，这里我们只使用 5 位。

我们还没有定义`R`和`2R`的值，这里有两种不同的方法，但由于很难找到精确到两个因数的电阻，我们将自己制作。只是为了使电路在试验板上更紧凑，我选择了 50k 的`R`和 100k 欧姆的`2R`。但是你没有任何精确的 50k 欧姆电阻？并联使用两个 100k 欧姆的电阻。这样，你只需要一种类型的电阻就可以完成所有的工作。

实际上，将两个电阻组合起来获得另一个值还有一个好处:这两个值基本上是平均的。如果一个“100k”电阻实际测量值为 101k，另一个测量值为 99k，那么它们的串联组合正好是 200k，并联组合正好是 50k。简而言之，只要平均值正确，使用这样的倍数会有所帮助。

最后，请注意，如果愿意，这些固定电阻都可以用电位计代替。特别是，用一个 100k 的电位计代替任何 50k 的“电阻”,会给你的输出波形提供一个有趣的可调度，如下所示。原则上，我们可以只用电位计制作一个完整的 R-2R DAC，小心地拨动电位计，使一侧的读数是另一侧的两倍。实际上，这种方法适用于三个或四个电位计，但之后就会失效，因为电位计的额定精度通常约为 5%或更低。尽管如此，对于从四个二进制输入产生奇数、适度可调的电压来说，这是一个有趣的技巧。

### 减轻

但是我们还没完。如果你继续使用这种 Thévenin 等效电路逻辑，直到最后一级，你会发现它(像它之前的每一级)有一个 50k 欧姆的等效电阻。这是一个很大的数目，这意味着在电压没有显著下降的情况下，我们无法从 DAC 中提取太多电流。所以在我们直接使用它之前，我们必须缓冲它，比如说把它交给你的有源扬声器。

虽然你完全可以使用一个[晶体管缓冲电路](https://en.wikipedia.org/wiki/Common_collector)，但我们会损失大约 0.6 伏的基极-发射极偏置电压。见鬼，这是逻辑噪音。所以拿出 4069UB 芯片，我们从[开始就一直用它来做线性缓冲。](http://hackaday.com/2015/03/09/logic-noise-sawing-away-with-analog-waveforms/)

[![quick_buffer.sch](img/e87de788a58ea80e3e5d3afbbf48f6ba.png)](https://hackaday.com/wp-content/uploads/2015/10/quick_buffer-sch.png)

我在反馈环路中用一个电位计构建了缓冲，以便您可以改变输出电平，我还在输出端展示了一个可选的低通滤波器，它可以抑制我们将要创建的波形中的一些剩余数字字符。与 4069 放大器电路一样，我们可以通过放大信号直到它开始软限幅来获得良好的过驱效果。

## 数字锯齿波

 [https://www.youtube.com/embed/jkICPvHmSDg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jkICPvHmSDg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



如果 R-2R DAC 提供的电压随着输入越来越大的二进制数而增加，用输入位上的逻辑高值表示，我们可以利用它来产生精确的锯齿波形。在[早期的逻辑噪声](http://hackaday.com/2015/03/09/logic-noise-sawing-away-with-analog-waveforms/)中，我们通过添加一个二极管，从我们的标准振荡器构建了一个“锯齿”波形。但老实说，这是一个相当蹩脚的锯齿。

[![old_sawtooth_scope](img/f9f13040c3c818c92b8d8a5540314832.png)](https://hackaday.com/wp-content/uploads/2015/10/old_sawtooth_scope.png) 因为电路中真正发生的是电容器的指数衰减，所以它基本上是一个摇摆锯齿波。但现在我们能够相当直接地将数字转换成电压，我们可以产生非常精确的锯齿波，如果你喜欢的话。

[![scope_59](img/2f4374c152113e10353d80e8c7506b93.png)](https://hackaday.com/wp-content/uploads/2015/10/scope_59.png) 秘密在于计数，为此我们将翻出一个我们以前用过的 4040 二进制计数器芯片。当一个时钟脉冲进入计数器时，它的各种输出代表到目前为止到达的脉冲数。将这个二进制数输入我们的 DAC，我们得到一个简单的上升电压。上坡波。

现在，我们将斜坡馈入反相缓冲电路，在另一端得到一个漂亮的锯齿波。如果你想过滤，你可以。它消除了一些来自离散电压电平之间跳变的高频噪声。很明显，所以你应该看你更喜欢哪种方式。

[![logic_sawtooth.sch](img/b9244580adb2588181bf385015c57684.png)](https://hackaday.com/wp-content/uploads/2015/10/logic_sawtooth-sch.png)

### 数字疯狂

上述电路有两种互补的思考方式。一是我们使用计数器芯片进行二进制计数，并将二进制数值输入 DAC。另一个更具模拟/音乐性的观点是，我们将五个方波发送到一个分压器，每个方波相隔一个八度音程，分压器将每个方波的音量减半。将这些以“正确”的顺序堆叠起来，我们就得到一个斜坡波形。

但是，当不同的方波进入 DAC 时，对它们进行转换，会使声音中包含更多高频成分。现在，频率最低的方波(最高有效位)是最大的。把最高和最低的投入交换一下，你就明白我的意思了。

[![illustrative_matrix](img/03873c2b77a6cac3b6d72c9ce63c7bd8.png)](https://hackaday.com/wp-content/uploads/2015/10/illustrative_matrix.png)

这种实现的有趣之处在于，你有办法(以数字方式)改变输出波形的音色，方法是打乱 DAC 的输入，或者完全丢弃特定的 DAC 输入。这就是你在简介中看到的最后一个电路。一个 4066 开关(参见[逻辑噪声:乒乓立体声](http://hackaday.com/2015/07/02/logic-noise-ping-pong-stereo-mixers-and-more/)，文章中途)通过来自 4040 计数器的时钟的进一步细分来开关四个最高音调方波输入。

但是也有其他方法来改变音色。有了足够的 4051 多路复用器芯片，您可以将多个方波重新路由到每个 DAC 输入。或者将移位寄存器回路的输出馈入 DAC。如何驾驶所有这些取决于你自己。

## 结论

如果你已经建立了本次会议的 DAC 电路，不要撕毁它。在下一版中，我们将把 DAC 和 VCO 结合起来，并对它们进行调整。像这样调整电路是很棘手的，我们可能需要稍微改变一下唯一逻辑芯片的规则，但这是值得的，因为我有一个很棒的移位寄存器加 DAC 加 VCO 电路可以展示给大家。