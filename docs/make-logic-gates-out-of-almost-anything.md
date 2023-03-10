# 用(几乎)任何东西制造逻辑门

> 原文：<https://hackaday.com/2017/01/03/make-logic-gates-out-of-almost-anything/>

逻辑门是数字电子设备的基础，它对一个或多个二进制输入进行逻辑运算，产生单个输出。这些操作使得你拥有的每一个设备中的所有计算成为可能，无论是你的手机、电脑、游戏机等等。实现逻辑门有无数种方式；机械地、电子地、虚拟地(想想《我的世界》)等等。让我们看看如何创建一些有趣的、与众不同的 gate 实现。

### 它们是如何工作的

作为一个例子，让我们考虑与门(其他的是或、非、与非、或非、异或和![andgate](img/4099eb3fe5babcdafccdb6efa8029938.png) XNOR)。电子门在两个标称电压下工作，通常是 0 V 和 5 V，分别代表逻辑 0 和逻辑 1。

与门有两个输入 A 和 B。根据右边的真值表，与门的输出 A.B 取决于这两个输入。只有当 A *和* B 都为 1 时，与门才有“1”输出。正如你所猜测的，当 A *或* B 为 1 时，或门输出为 1，只有当 A 和 B 都为 0 时，或门输出为 0。

每个门都有自己的真值表。虽然这七个门通常被认为是“基本”门，但也有一些门，如与非门，是通用的，这意味着它们可以相互连接来构建所有其他的门。

### 组合门

逻辑门可以组合起来执行任何计算。一个电脑芯片里有几百万个这样的东西。但是让我们来看一个非常简单的与门的应用。

左边是自动恒温器的示意图。如果水很冷，加热器必须打开，但前提是水箱中有足够的水。触点 X 和 Y 靠近水箱顶部，如果它们被水覆盖，信号将被发送到门的一个输入端。热敏电阻感应水温，如果水温足够低，就会向另一个门输入端发送信号。因此，当有足够的水*和*温度足够低时，加热器继续工作。

### 其他门实现

当代逻辑电路使用 MOSFETs 作为构建门的元件，但有许多方法来实现它们。使用继电器是其中之一，你可以看到它们是如何工作的。[Andrew Kingsolver]在解释基于继电器的逻辑方面做得非常出色。下图显示了他对 AND 和 OR 门的实现。对电路的快速分析揭示了真值表是如何从由两个开关代表的输入中获得的(给继电器中的线圈通电会将触点推到远极)。

 [![relay-and-gate](img/08029423a98d880e0b4993a8fedb9934.png "relay-and-gate")](https://hackaday.com/2017/01/03/make-logic-gates-out-of-almost-anything/relay-and-gate/)  [![relay-or-gate](img/59e3124f0455d5a313196069e38560b8.png "relay-or-gate")](https://hackaday.com/2017/01/03/make-logic-gates-out-of-almost-anything/relay-or-gate/) 

为了理解如何用逻辑门进行运算，半加法器是一个很好的例子。[【安德鲁·金索弗】也做到了](http://www.andrewkingsolver.com/relay-full-adder-circuit/)。它有两个输入(0 或 1 ),输出一个和，一个进位，当然是二进制的。这可以用与门和异或门来实现。你可能知道，[早期的计算机](https://en.wikipedia.org/wiki/History_of_computing_hardware#Electromechanical_computers)是基于中继的，如果你有时间的话，[甚至可以做一个只是为了好玩的](http://hackaday.com/2010/11/18/electromechanical-computer-built-from-relays/)。

![](img/a2b17f1f7d41abc2f25a1b6f6dc8ae4b.png)

真空管取代继电器成为计算的主要元件。实现 NOR 逻辑门的简化电路，当两个输入都为 0 时，仅输出 1，如右图所示。管栅是输入。当两个栅极都处于低电平时，没有输出，因为电流流向地。当电压施加到两个栅极时，电子管基本上变成无穷大电阻，电流流向输出端。

和继电器一样，各种逻辑电路都是用真空管制成的。在 ENIAC 计算机中有 17468 个。与继电器相比，电子管电路体积更大，耗电量更大，但计算速度要快得多。

 [![Early vacuum-tube memory modules, circa 1955.](img/336965c35774e8cda31c3adf68049539.png "pluggable_memory_module")](https://hackaday.com/2017/01/03/make-logic-gates-out-of-almost-anything/pluggable_memory_module/) Early vacuum-tube memory modules, circa 1955\. [![Diode AND gate by Thingmaker, CC-BY-SA 4.0](img/b38dbdb4148ec431d28b1c46e7c1f507.png "640px-diode_and2_ideal_diode")](https://hackaday.com/2017/01/03/make-logic-gates-out-of-almost-anything/640px-diode_and2_ideal_diode/) Diode AND gate [by Thingmaker](https://commons.wikimedia.org/wiki/File:Diode_AND2_Ideal_Diode.jpg), CC-BY-SA 4.0

最终，硅出现了，真空管逻辑被二极管和晶体管逻辑取代。这意味着速度大幅提高，尺寸和功耗大幅降低。你猜对了，二极管也可以用来建造逻辑门，但不是全部，只有 AND 和 OR 门可以只用二极管建造。然而，通过添加晶体管作为有源元件，可以实现所有其他的门。

上图所示为三输入、二极管专用与门。当所有输入都为正时，电流将流过电阻，并将输出拉向正。如果三路输入中的任何一路为 0 伏，流过相应二极管的电流会将输出电压拉低至 0 伏。其他二极管将被反向偏置并且不传导电流。

机械逻辑门怎么样？当然，你可以[用乐高](https://www.youtube.com/watch?v=5X_Ft4YR_wU)建造大门和一个半加法器，或者用[木头和大理石](https://www.youtube.com/watch?v=GcDshWmhF4A)建造一个小型加法器。当然，也可以设计[气动](https://www.youtube.com/watch?v=BX2XfIID7l0)逻辑门(在湿度或灰尘高的地方很有用)。

![orms](img/13aa730c02d0d19300e35a494dd01eb4.png)

OR gate built in Minesweeper

也存在一些奇怪的建造逻辑门的方法。康威的[生命游戏](https://en.wikipedia.org/wiki/Conway%27s_Game_of_Life)，也许是最著名的细胞自动机，已经被证明是一个通用的图灵机，这意味着任何可以通过算法计算的事情都可以在游戏中完成。游戏本身就很吸引人，游戏中建造大门的详细方法[已经在](http://www.rennard.org/alife/CollisionBasedRennard.pdf)中描述过了。

另一个类似的[例子来自扫雷游戏](http://www.formauri.es/personal/pgimeno/compurec/Minesweeper.php)，在早期版本的 Windows 中很流行。这个游戏看似无辜，但实际上是一个 [NP 完全](https://en.wikipedia.org/wiki/NP-completeness)问题(最难解决的问题)。

所以如果你有一些空余时间，可以考虑造一些逻辑门，毕竟有很多方法可以做到！