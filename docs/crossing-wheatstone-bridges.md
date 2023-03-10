# 交叉惠斯通电桥

> 原文：<https://hackaday.com/2016/11/08/crossing-wheatstone-bridges/>

惠斯通电桥是一种非常精确的测量电阻的方法，尽管它在 150 多年前就被发明了，但它今天仍然被广泛使用。甚至在 Hackaday 上搜索它也会在许多黑客活动中使用它。这是一个基本的实验装置，你应该知道。

## 它是如何工作的

![Balanced series resistors](img/ca9a9a7b6fc8d77204ad001bb2254643.png)

Balanced series resistors

这里有一个简单的方法来理解惠斯通电桥的工作原理。原理图中有两个分压器(成对串联的电阻):R1 和 R2，R3 和 R4。如果你算一下，你会发现 R1 和 R3 两端的电压是一样的，R2 和 R4 的电压也是一样的。这是因为电阻 R2/R1 的比值与电阻 R4/R3 的比值相同。两者都形成分压器网络，并且都以相同的方式分压。

但关键是，如果我们要测量 A 点和 C 点之间的电压，你会看到它们之间的电压为 0 伏，没有电流流动。此时，我们说惠斯通电桥是平衡的。

 [![Wheatstone bridge with one unknown](img/9ce98dc7b0aa29b2ed84decae1c003f8.png "Wheatstone bridge with one unknown")](https://hackaday.com/2016/11/08/crossing-wheatstone-bridges/wheatstone_bridge_how_it_works_2/) Wheatstone bridge with one unknown [![Wheatstone bridge with potentiometer](img/013b6daa31f137118442416b8840d8ef.png "Wheatstone bridge with potentiometer")](https://hackaday.com/2016/11/08/crossing-wheatstone-bridges/wheatstone_bridge_how_it_works_3/) Wheatstone bridge with potentiometer

现在让我们说我们不知道 R4 的电阻(让我们称它为 Rx)。让我们通过如上所示的检流计连接 A 和 C。如果电流是 0 安培，那么我们可以找到 Rx 的值。这是因为，正如我们上面所说的，当 A 和 C 之间没有电流流动时，R2/R1 之比必须等于 Rx/R3 之比。重新排列，我们得到 Rx = (R2*R3)/R1，求解，我们得到(8*6)/4=12 欧姆。

但是如果 A 和 C 之间有电流流动呢，或者我们可以问，如果 A 和 C 之间有电压呢？在这种情况下，我们将 R2 从固定值电阻改为电位计，如上面的第二张图所示。请注意，B 点和 D 点实际上在电学上是相同的，因此我们可以将它们设为同一点，并以惠斯通电桥更常见的菱形重新绘制原理图。当我们打开电路时，检流计可能会显示 A 和 c 之间的电流。然后我们会调整 R2 值，直到检流计显示没有电流。然后，我们可以测量 R2 的电阻，得到 8 欧姆，然后再次进行上述计算，看到 Rx 是 12 欧姆。

 [![Wheatstone bridge on breadboard setup](img/c7c5ffc230491b0aca3d258e94b01d94.png "wheatstone_bridge_on_breadboard_setup_an_bright")](https://hackaday.com/wheatstone_bridge_on_breadboard_setup_an_bright/) Wheatstone bridge on breadboard setup [![Wheatstone bridge on breadboard](img/54af4f49c1e65f520d6d0b46d4447f3c.png "wheatstone_bridge_on_breadboard_an_bright")](https://hackaday.com/wheatstone_bridge_on_breadboard_an_bright/) Wheatstone bridge on breadboard

事实上，这正是我所做的，如照片所示，以尝试它。当然毫无疑问，这是可行的，但我无法抗拒(明白吗？)亲眼所见。

但是问题来了，如果我们能测量 R2，那么为什么我们不能测量 Rx 呢？Rx 可能是一个集成在建筑物中的应变仪，所以我们无法测量它。我们将在下面看到更多的应变仪。或者，电阻的变化可能非常小，以至于我们的电表不可靠，在这种情况下，我们实际上是在放大和测量电压，但我们也将在下面讨论这一点。

## 应变仪中的惠斯通电桥

![Wheatstone bridge with strain gauge](img/168a06a81f54eeaa5d8b33402e174648.png)

Wheatstone bridge with strain gauge

由于惠斯通电桥能够测量非常小的电阻变化，因此它经常用于测量应变仪上的应变。这些检测建筑物、桥梁和其他结构的变化。

图为惠斯通电桥，应变计为 R4。拉伸应变仪会引起电阻的变化，因此应变仪是一个可变电阻。一个、两个或所有四个电阻可以是应变仪，电桥分别称为四分之一桥、半桥或全桥惠斯通电桥电路。

请注意，电压输出 V [O] 非常小，需要放大才能被其他电路使用。该公式显示了 V [O] 与激励电压、V [E] 和电阻的关系。

![Tension bars and strain gauges on a bicycle crank](img/04dd0b7d909c8b557e87a0f013fd6c1a.png)

Tension bars and strain gauges on a bicycle crank

图中所示为内置应变仪的张力杆，用于测量应变。只有一个应变计的是四分之一电桥。

另一个拉杆有两个应变计，半桥也是如此。然而，R3 不与应变材料结合，因此不会受到应变的影响。相反，R3 的作用是补偿温度变化的影响。温度变化会导致两者膨胀或收缩，但由于温度变化对两者的影响相同，因此两者的电阻比将保持不变，不会影响输出电压。这样，只有由于 R4 应变引起的电阻变化才会影响输出电压。在照片中，你可以看到相同配置的应变仪[粘在自行车曲柄](https://hackaday.com/2016/04/03/bike-power-meter-with-crank-mounted-wifi-strain-gauges/)上。

应变用ε(希腊字母ε)表示，应变和电阻变化之间的关系由该公式定义。

![Strain and resistance relationship](img/bb772436c7c06b082022e5e67f6c3056.png)

在那里，电阻的变化与应变和应变计系数 k 有关，该系数是应变计的一个特性，并已从实验中导出。以上内容超出了本文的范围，但可以在关于应用惠斯通电桥的出版物中找到。

## 测量微小的温度变化

![Wheatstone bridge with thermistor for temperature](img/53adff7042f30f6a85be5b47b6fb0614.png)

Wheatstone bridge with thermistor for temperature

用惠斯通电桥和热敏电阻器可以测量微小的温度变化。热敏电阻是一种电阻随温度变化的电气元件。如图所示，我们将热敏电阻放在电桥中，作为要测量其值的电阻，尽管我们不直接测量。

在这种情况下，我们没有平衡桥梁。相反，我们直接使用电桥两端的差分电压 V [O] 。V [O] 与热敏电阻的电阻 Rt 成正比，并映射到温度。

需要注意的一点是，过高的电流会导致热敏电阻额外发热。在这种情况下，我们保持低激励电压。但是这导致输出电压 V [O] 也变低。我们通过在输出端后放置一个放大器来解决这个问题。

热敏电阻的电阻与温度的关系也是非线性的。如果使用的温度范围很小，那就不是问题了。然而，一些热敏电阻制造商给出了他们的热敏电阻何时用于惠斯通电桥的公式，就像[这个](http://www.ametherm.com/thermistor/ntc-thermistors-temperature-measurement-with-wheatstone-bridge)一样。

## 寻找地下断层——默里回路测试

![Murray loop test](img/29ef9d24f51ca5e7c89dd34eeacd3892.png)

Murray loop test

默里回路测试是一种使用惠斯通电桥来寻找地下线路中故障位置的方法，而不必先挖掘。进行测试的一种方法是使用所示的设置。有故障的电缆是地下的电缆，沿其长度在某个未知位置有接地故障。使用电阻足够低的电线将声音电缆连接到故障电缆，从而不会影响测试。

Lx 是所示故障电缆一部分的未知长度，其电阻为 Rx(也是未知的)。l 是已知的声音电缆和故障电缆的组合长度。如果完好电缆和故障电缆的横截面积相同，则两个导体的电阻与其长度成正比。这允许我们在倒数第二个方程中进行代入，得到最终的方程，求解 Lx，如图所示。

对于惠斯通电桥，我们首先必须平衡电桥，这意味着通过检流计的电流必须为零。这是当第一个等式中的比率为真时，因此其余的等式也为真。但是一旦平衡了，我们知道 R1，R2 和 L，我们就能解出 Lx。知道了长度 Lx，就知道从哪里挖修复故障了。

## 结论

我们说过你可以在这里找到惠斯通电桥。其中一个就是这个使用应变计从头开始制作的[数字秤。另一个是这个](http://hackaday.com/2013/06/12/building-a-digital-scale-from-scratch/)[自行车功率计，应变仪粘在踏板曲柄](http://hackaday.com/2016/04/03/bike-power-meter-with-crank-mounted-wifi-strain-gauges/)上，包括上面描述的温度补偿仪。

我们可以继续谈论惠斯通电桥的用途。例如，我们还没有讨论它在交流应用和测量电容和电感中的用途。也许我们下次再讨论这个问题。现在，我们很想听听你在测量电阻中使用惠斯通电桥的情况，以及你想从你的经验中补充的任何其他情况。