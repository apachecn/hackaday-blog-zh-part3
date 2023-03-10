# 以毫米为单位测量高压(以及其他高压探头技巧)

> 原文：<https://hackaday.com/2016/12/08/measuring-high-voltage-in-millimeters-and-other-hv-probe-tricks/>

我经常在高压下工作，其他人经常重复我的项目，所以我经常被问到“需要什么电压？”。这意味着我需要能够测量高电压。以下是我如何使用福禄克高压探头以及我自己自制的探头来做这件事。如果你没有探针呢？我也有解决办法。

## 你的火花有多长？

测量高电压最简单的方法是通过火花长度。如果你的电路有火花隙，那么当火花出现时，那就是短路，将你积累的电荷全部倾倒。当你的火花间隙在你获得火花的最大距离时，那么就在火花发生之前，你有你的最大电压。在火花期间，电压迅速变为零，根据你的电路，它可能会再次开始建立。火花发生前的电压与火花长度有关，火花长度也是火花间隙宽度。

下面的示波器照片显示了这个变化的电压。这种方法适用于粗略估计。当我在下面讨论高压探头时，我会谈到如何进行更精确的测量。

但事情没那么简单。电极的形状起着很大的作用，间隙中通常是空气的压力和温度也是如此。对于扁平电极或直径明显大于间隙尺寸的球形电极，在 25C (77F)的空气中，可以使用以下公式:

```
voltage (kV) = 3 x pressure x spark length + 1.3√spark length
```

压力的单位是大气压，火花长度的单位是毫米。大多数黑客在 1 个大气压下工作，所以可以不考虑这个公式。此外，对于一个 10 毫米的火花隙，例如，10 毫米的平方根乘以 1.3 意味着你增加了一个微不足道的 4.1。所以这个公式通常被简化为:

```
voltage (kV) = 3 x spark length (in mm)
```

或厘米:

```
voltage (kV) = 30 x spark length (in cm)
```

这只是 30kV/cm 的另一种说法。对于英寸，公式为:

```
voltage (kV) = 76.2 x spark length (in inches)
voltage (kV) = 11.8 x spark length (in inches)
```

 [![Spark length measuring setup](img/ddf73a1a7ecd2f4efa84da9a7bbba1bc.png "Spark length measuring setup")](https://hackaday.com/2016/12/08/measuring-high-voltage-in-millimeters-and-other-hv-probe-tricks/spark_length_measuring_setup_with_fluke_clean_wires/) Spark length measuring setup [![Measuring spark length](img/dde5c8246416f0f777b7eb8ac81bcc25.png "Measuring spark length")](https://hackaday.com/2016/12/08/measuring-high-voltage-in-millimeters-and-other-hv-probe-tricks/measuring_spark_length/) Measuring spark length [![Spark gap and oscilloscope](img/78e895633188042d1279a59cd3ffbe07.png "Spark gap and oscilloscope")](https://hackaday.com/2016/12/08/measuring-high-voltage-in-millimeters-and-other-hv-probe-tricks/spark_gap_and_oscilloscope_an/) Spark gap and oscilloscope

在上面的照片中，测得的电压是 17kV。火花隙宽度(即火花长度)测量值略低于 5 毫米。如果我们应用 5 毫米火花隙的公式，我们得到 3×5 毫米= 15kV。对于某一电压范围，球体越大，测量值应该越接近公式，但在下面会更接近公式。

然而，如果您使用更尖锐的电极，如针或棒，那么在足够的电压下，电极之间的电场将会更不均匀，并且在某些地方会强到足以电离间隙中的一些空气。这实质上造成了高电阻短路，这意味着你的电压将会降低。上述公式将不再适用。在这种情况下，你可以试着在图表中查找你的火花长度和电极配置。

![Spark gap width to voltage chart](img/7521e82f03a2d2409d0b87b1659a1559.png)

Spark gap width to voltage chart

上面的图表总结了所有这些。深蓝色的底线是根据公式(本质上是 30kV/cm)的线:

```
voltage (kV) = 30 x spark length (in cm)
```

该公式定义了火花长度和电压之间的线性关系。看起来在 50kV 处有一个向上的弯曲，但这是因为 50kV 以下的电压等级增加 5，50kV 以上增加 10。上面是真实的数据。如你所见，针状电极最不符合公式。球体直径越大，在它们不再紧密跟随 30kV/cm 线之前，它们达到的电压越高。这些天来，我的大部分工作都在 30kV 以下，尽管我的电极很少像大多数黑客那样是大球体。除非你正在使用范德格拉夫发电机，但即使这样，通常也只有圆顶是球形的，其他电极不是。

## 使用福禄克高压探头

![The Fluke 80K-40 HV probe](img/a24063ec592c9884d44f6ee8bf835930.png)

The Fluke 80K-40 HV probe

为了更精确的测量，我使用了福禄克 80K-40 高压探头。这款设计用于 1kV 至 40kV DC，精度根据温度从 1%到 2%不等，不包括电表的精度。对于交流，它设计用于峰值交流，20kV RMS，并在 60Hz 时提供+/-5%的精度。输入电阻为 1000M。它与上面照片中的 10Mω+/-1.0%电压表或示波器一起使用。借助外部分流器或校正系数，可以使用具有其他阻抗的仪表，所有这些都在探头文档中有所描述。

进行测量时，读取仪表或示波器上的读数，并乘以 1000。这就是我如何从示波器上显示的 17V 到上面例子中的 17kV。

 [![Measuring voltage for a smoke precipitator](img/68f031f494666eb6651e78135e9fd884.png "Measuring voltage for a smoke precipitator")](https://hackaday.com/2016/12/08/measuring-high-voltage-in-millimeters-and-other-hv-probe-tricks/fluke_80k_40_probe_and_smoke_precipitator/) Measuring voltage for a smoke precipitator [![Measuring voltage for a lifter](img/7be36c8f4bd39613118fc4f9db7a1514.png "Measuring voltage for a lifter")](https://hackaday.com/2016/12/08/measuring-high-voltage-in-millimeters-and-other-hv-probe-tricks/fluke_80k_40_probe_and_lifter/) Measuring voltage for a lifter

这里有两张我使用福禄克探针的照片。一个是 10MωFET 模拟表，用于测量烟尘除尘器两端的电压[。另一个是模拟仪表，但我手里拿着探头。我正在测量由](http://hackaday.com/2014/03/13/cleaning-up-smoke-with-an-electrostatic-precipitator)[电脑显示器电源](http://hackaday.com/2014/06/14/repurpose-an-old-crt-computer-monitor-as-a-high-voltage-science-project-power-supply)提供的升降机两端的电压。

## 自制高压探头

![Using the DIY high voltage probe](img/b72afdb5d32b33b1065768b7ad78ce00.png)

Using the DIY high voltage probe

福禄克是好的高达 40 千伏 DC，但我必须测量更高，所以我自己做了探头。我用过的最高电压是 75 千伏的 DC，尽管它的电表最高设计电压是 150 伏，相当于 150 千伏的输入电压。

![High voltage probe design](img/b2d24382ef1ded149821e37308336bfa.png)

High voltage probe design

以上是如何设计的。与电表的 10mω阻抗(R3)和电表正在测量的电阻(也是 10mω，R2)相比，R1 的电阻非常高。没有 R2 也能做到，但这会给电表带来高电压的危险。

R2 和 R3 是并联的两个电阻，组合起来可以算作一个 5Mω电阻，如图中的第一个公式所示。它们通常一起被命名为 R2||R3。右边的示意图是观察 R3 从电表中拉出并与 R2 相结合的电路的简化方法。

R1 和 R2||R3 形成一个分压器。图中的第二个公式显示了 R2||R3 两端的电压是如何计算的。请注意，结果 74.9V 几乎是被测电压 75，000V 的 1/1000。只差 0.1%，比米精度还小。这意味着我们可以说，要获得实际电压，只需将测得的电压乘以 1000 (75V x 1000 = 75，000V)。

选择 R1 的值，使其不会给被测电路带来负载。高压电路通常没有多余的电流用于测量。R1 也被选中，这样它的表面就不会有泄漏的问题。在我的例子中，R1 由 25 个较小的电阻组成，因此电压在它们之间分配，我认为不会有泄漏问题。最后选择 R1，以便 R2||R3 将有一个有用的电压范围。3000V 测量为 3V，20,000V 测量为 20V，75,000V 测量为 75V，等等，都是一个电表的合理数值。

![DIY HV probe resistors waxed](img/a91fd57426da9ced3226cca8abd09618.png)

DIY HV probe resistors waxed

对于 R1，我从 [Caddock](http://www.caddock.com) 购买了 25 个 200mω高压电阻器(MX440-200M，1%，11kV)并将它们串联起来。事后看来，我应该选择更高的电阻，但更长的电阻会使探针更短。

 [![Safety spark gaps](img/6622e7ccf85fc2ed65c579aaec9a72a0.png "Safety spark gaps")](https://hackaday.com/2016/12/08/measuring-high-voltage-in-millimeters-and-other-hv-probe-tricks/dit_hv_probe_safety_spark_gaps/) Safety spark gaps [![DIY HV probe's endcap and terminals](img/b7759ba309630835dd2970ebdb66fbc1.png "DIY HV probe's endcap and terminals")](https://hackaday.com/2016/12/08/measuring-high-voltage-in-millimeters-and-other-hv-probe-tricks/diy_hv_probe_endcap_label/) DIY HV probe’s endcap and terminals

电阻都是用又大又圆的焊料球焊接在一起的，以避免尖点，尖点会因电离而导致损耗。然后将每个接头装入模具中，倒入石蜡以进一步减少损失。

为了保护电表不受高压影响，我在里面加了两个火花隙，以防某些电阻短路。这方面的[计算](http://rimstar.org/zoltans/coronaring.htm)非常复杂，所以我不会在这里赘述。从照片中你可以看到它们由圆形的焊料球组成，与两个电阻的金属端盖相隔精确的距离。

## 结论

这就是我测量高电压的方法。我很好奇你是怎么做到的，你会推荐什么样的探测器，你有什么样的体验。还有，你做过交流电压测量吗？那是我没做过的事。我想到了测量特斯拉线圈的电压。请在下面的评论中告诉我们。