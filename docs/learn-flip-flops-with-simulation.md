# 通过模拟学习触发器

> 原文：<https://hackaday.com/2015/09/23/learn-flip-flops-with-simulation/>

使用 AND、OR 和 NOT 等组合门的数字设计相对简单。特别是，当你用这些门构成组合逻辑时，输出只取决于输入。输出的先前状态在组合逻辑中并不重要。虽然这很简单，但它也阻止了您构建像状态机、计数器甚至 CPU 这样的东西。

用自己的输出作为输入的电路称为时序电路。的确，在基本层面上，时序电路使用传统的逻辑门。然而，你通常不会把它们当作门来处理，而是会处理一些抽象的东西，比如锁存器、触发器，甚至更高级别的构造。了解这些更高层次的构造将使您能够做出更先进、更稳健的数字设计。事实上，如果你使用 FPGA，像触发器这样的构建模块是必不可少的，因为芯片的很大一部分是由某种触发器组成的。

为了更好地理解，我想以三种不同的方式来看顺序构建模块:在抽象级别，在门级别，然后像使用 FPGA 开发一样使用 Verilog。我将使用两个在线工具来模拟电路。首先是优秀的 Falsted 模拟器(现在使用 Javascript，所以会在更多的浏览器上运行)。它可以很容易地显示行为和门级操作。EDAPlayground 将让你在 Verilog 中模拟同样的电路。如果你还不想处理 Verilog，你可以安全地跳过这些部分和仿真，因为相同的材料将有逻辑门等效。这两者都不需要安装任何软件，只需要一个相当现代的浏览器。

然而，这意味着你不应该被动地阅读这篇文章。点击链接，尝试模拟！如果你想先复习一下组合门，[Bill Herd] [有一篇很棒的文章](http://hackaday.com/2015/05/28/from-gates-to-fpgas-part-1-basic-logic/)，你会喜欢的。

## 关于现实世界

理论上，我们的电路是完美的。电线没有电阻，电流瞬间从一个地方流向另一个地方。这有利于一般分析，因为真实导线的电阻很小，在我们大多数人工作的距离内，光速通常或多或少是瞬间的。

然而，重要的是要认识到这些近似值并不是真实世界的工作方式。在某些情况下，我们将利用现实世界的影响，在其他情况下，我们将不得不理解它们，以确保我们的电路工作。

比如看下面的电路。它是做什么的？理论上，它什么也不做。一个与门必须有两个真输入才能有一个真输出，因为一个输入总是另一个的反相，这不可能发生，对吗？

[![](img/1669aef81a50082d287410be6d372735.png)](https://hackaday.com/wp-content/uploads/2015/09/circ11.png)

事实上，它可以，但只是因为电路元件不像我们希望的那样完美。当逆变器的输入改变时，输出不会立即改变。部分原因是输出电路的电容。其他延迟是由实现反相器的任何元件(例如，晶体管、继电器或 MOSFET)的特定物理效应造成的。

考虑输入从低到高之前的时间。投入低，已经很久了。反相器的输出为高，因此与门输出 0。现在，输入变为高电平或真状态。反相器最终会输出 0，但不是立即输出。在此之前(假设导线传送信号变化的时间比反相器的传播延迟小得多)，与门将输出 1(当然，在它自己的传播延迟之后)。这就形成了一个基本的上升沿检测器。输出脉冲的宽度将取决于通过逆变器的延迟。无论输入保持高电平多长时间，输出端都只有一个短脉冲。

在现实生活中，您可能希望让反相器实际上非常慢，以便从检波器获得特定的脉冲宽度，并抵消与门的延迟。例如，你可以用一个 RC 网络来延长时间。你也可以使用奇数个反相器。如果你正在设计一个 IC，你可以对器件的几何形状做一些事情来使它变慢。

在 [Falstad 模拟器(点击此链接模拟电路)](http://www.falstad.com/circuit/circuitjs.html?cct=$+1+0.000005+10.200277308269968+50+5+50%0AR+224+128+160+128+0+5+10+5+0+0+0.5%0A150+624+144+752+144+0+2+0%0AI+272+208+352+208+0+5.000000000000001e-7%0Aw+224+128+624+128+0%0Aw+224+128+224+208+0%0Aw+224+208+272+208+0%0Aw+624+160+624+208+0%0Aw+624+208+432+208+0%0Ax+285+254+477+257+0+24+Slew+rate+500nV/s%0Aw+352+208+432+208+0%0AM+752+144+832+144+0+2.5%0Ao+3+64+0+38+5+0.00009765625+0+-1+Input%0Ao+7+64+0+38+5+0.00009765625+0+-1+Post+inverter%0Ao+10+64+0+38+5+0.00009765625+0+-1+Output%0A)的情况下，我将逆变器的压摆率设置为 500 uv/秒。如果在示波器上观察反相器的输出，会发现输出边沿更像斜坡，这就是边沿检测器工作的原因。(注意:模拟器可能会将电路显示在屏幕的一侧，甚至可能完全显示在屏幕之外。要纠正这种情况，请从模拟器菜单中选择编辑|中心电路。)

在 Verilog 中有一个延迟语句，你可以用它来模拟这种行为。当您为 FPGA 进行综合时，您不能使用延迟语句，但工具确实知道 FPGA 电路的真正门延迟是什么，并将使用这些延迟。你不能改变他们。

事实上，Verilog 识别两种类型的延迟:惯性延迟(组件识别变化所需的时间)和传输延迟。有一篇很好的论文[介绍了如何在 Verilog](http://www-inst.eecs.berkeley.edu/~cs152/fa06/handouts/CummingsHDLCON1999_BehavioralDelays_Rev1_1.pdf) 中进行不同的延迟建模，但现在这里是 Verilog 中的[相同边沿检测器:](http://www.edaplayground.com/x/Tc7)

```
`default_nettype none
module edgedet(input a, output z);
reg b;
assign z=a&b;
always @(a)
 b<=#2 ~a;
endmodule
```

assign 语句相当于与门，always 模块是具有 2 个时钟周期传输延迟的反相器。然而，我的观点不是如何制作边缘检测器。我的观点是，现实生活中的延迟是可以被利用的(尽管它们也会引起问题)。

## 时序和时钟逻辑的情况

显而易见，时序逻辑对于任何有记忆的事物都是必要的。然而，你会发现几乎所有真实世界的设计都使用一种特定的模式。组合逻辑的每一位将从使用时钟的触发器获得输入。输出将到达同一时钟上的其它触发器。反过来，这些触发器将驱动其他门输入。这就是所谓的同步逻辑。

理论上，你不必这样做。然而，如果你不这样做，你就要求做更多的工作。考虑下面的场景。对于工业控制项目，如果传感器输入“B”变高，您需要快速关断电源，除非传感器“A”同时也变高。定义这一点最简单的方法是用一个与门输入“B”和输入“A”的反相(当然，有许多方法可以做到这一点；这不是重点)。

[下面是一个模拟电路，也有一个慢速反相器](http://www.falstad.com/circuit/circuitjs.html?cct=$+1+0.000005+10.200277308269968+50+5+50%0AI+432+160+512+160+0+5e-7%0Aw+432+160+416+160+0%0A150+544+176+656+176+0+2+0%0Aw+512+160+544+160+0%0Aw+416+208+544+208+0%0Aw+544+208+544+192+0%0AS+416+208+320+208+0+0+false+0%0AL+320+160+272+160+0+0+false+5+0%0Aw+416+160+320+160+0%0Aw+320+160+320+192+0%0AL+320+224+272+224+0+0+false+5+0%0AM+656+176+736+176+0+2.5%0Ao+7+64+0+39+0.0000762939453125+0.00009765625+0+-1+Input+A%0Ao+10+64+0+39+0.0000762939453125+0.00009765625+0+-1+Input+B%0Ao+11+64+0+38+0.0000762939453125+0.00009765625+0+-1+Output%0A)。如果你把开关放在下面的位置，你可以分别控制 A 和 B。如果您向上扳动开关，则顶部逻辑输入控制 A 和 B(单击 H 或 L 反转输入的状态)。当 A 和 B 同时从低电平变为高电平时，输出端会出现毛刺。如果这关闭了机器的电源，这将是一个错误。如果你愿意，你也可以在 Verilog 中找到[相同的型号。](http://www.edaplayground.com/x/Tve)

[![cir2](img/119e327500053c6361c0dbd0cf933013.png)](https://hackaday.com/wp-content/uploads/2015/09/cir2.png)

有了时钟和触发器，慢速反相器就没那么重要了。如果从输入到输出的最长延迟短于时钟频率，则毛刺不会出现在输出端。稍后我会详细讨论 D 触发器，但现在就把它想象成一个一位存储器。当时钟从低电平变为高电平时，输出变为 D 输入。在所有其他时间，输出不会改变。现在，如果 A 和 B 馈入 D 触发器，输出通过 D 触发器，毛刺仍可能发生，但它会在无人注意时发生(即不是在时钟边沿)。这可能是真的，如果一棵树倒在空旷的森林中，它仍然会发出声音，但没有被记录到触发器中的小故障就会消失。

[![circ3](img/989f02ee412b342e097cedb31973fbb4.png)](https://hackaday.com/wp-content/uploads/2015/09/circ3.png) 添加触发器使电路看起来像右边的那个。你可以[在模拟](http://www.falstad.com/circuit/circuitjs.html?cct=$+1+0.000005+10.200277308269968+50+5+50%0AI+464+160+544+160+0+5e-7%0A150+576+176+688+176+0+2+0%0Aw+544+160+576+160+0%0AS+224+112+128+112+0+1+false+0%0AL+128+64+80+64+0+1+false+5+0%0Aw+128+64+128+96+0%0AL+128+128+80+128+0+1+false+5+0%0A155+304+48+368+48+0+5%0A155+384+304+416+304+0+5%0A155+720+176+752+176+0+0%0Aw+400+48+448+48+0%0Aw+448+48+448+160+0%0Aw+448+160+464+160+0%0Aw+480+304+576+304+0%0Aw+576+304+576+192+0%0Aw+688+176+720+176+0%0AR+256+224+176+224+1+2+25+2.5+2.5+0+0.5%0Aw+256+224+256+80+0%0Aw+256+80+304+80+0%0Aw+256+224+256+336+0%0Aw+384+304+336+304+0%0Aw+336+304+336+192+0%0Aw+336+192+224+192+0%0Aw+224+192+224+112+0%0Aw+128+64+192+64+0%0Aw+192+64+192+48+0%0Aw+192+48+304+48+0%0Aw+256+336+384+336+0%0Aw+720+208+688+208+0%0Aw+688+208+688+224+0%0Aw+256+224+688+224+0%0AM+816+176+912+176+0+2.5%0Ao+4+64+0+39+5+0.00009765625+0+-1+Input+A%0Ao+6+64+0+39+5+0.00009765625+0+-1+Input+B%0Ao+16+64+0+39+5+0.00009765625+0+-1+Clock%0Ao+31+64+0+38+0.0000762939453125+0.00009765625+0+-1+Output%0A)中看到它是如何工作的(同样，把拨动开关向上，从 L 转到 H；您会在中间结果中看到毛刺，但不会在输出中看到)。如果你喜欢用 Verilog 进行[实验，你可以模拟同样的效果，尽管你可能要等到我们更多地讨论 Verilog 中的触发器才能从中获得最大的收益。不管怎样，你可能会注意到一些事情。如果输入太短(相对于时钟)，电路将忽略它。一般来说，时钟频率需要至少是您需要处理的最快输入的两倍。](http://www.edaplayground.com/x/X_6)

## 逻辑元素

希望现在，你同意这些触发器和时钟逻辑是一件好事。触发器和其他时序电路有很多变化。然而，有一些公认的名称涵盖了您需要的电路元件的基本类型。不过，细节可能会有所不同(例如，触发器可能在时钟的上升沿或下降沿激活)。其他输入可能以高电压为真，而其他输入使用低电压。不过，概念是相同的。

为了避免混淆，我将使用 asserted 这个词来代替 true。请记住，虽然置位通常意味着真或逻辑 1，但如果输入是低电平有效输入，也可能意味着 0。

有几个元素值得讨论:SR，D，T，JK 触发器。在这四个中，有一个(SR)通常不计时(通常称为锁存器)。其他三个(D、T 和 JK)有时钟输入，尽管有时会看到锁存器版本，尤其是 D 触发器。你很快就会看到不同之处。

## 触发器信号名称

[![ff](img/fd45dde43527a7f0664f626c325a9005.png)](https://hackaday.com/wp-content/uploads/2015/09/ff.png) 不管是哪种类型的人字拖，都有一些常见的事情需要注意。在一个示意符号中(见右图)，在触发器的盒子里会有一个小三角形。这是时钟输入。如果紧挨着三角形的盒子外面有一个小圆圈，那就是负沿~~或水平~~时钟(右图中没有)。(正如[Sheldon]在评论中指出的，从技术上讲，三角形只应该出现在边沿敏感时钟中，但错误使用该符号并不罕见，所以要小心。)

触发器的输出几乎总是被称为 Q。正如您将看到的，该设计通常免费产生反相输出，用 Q 表示，上面有一个横杠。在所有情况下，如果 Q 输出有效，Q-bar 输出无效，反之亦然。

你可能会发现有特殊功能的人字拖。例如，预设允许您强制 Q 输出为真，重置则强制为假。同步预置或复位仅在时钟有效时发生(即在有效时钟边沿或电平)。无论时钟如何，异步预置或复位都会立即发生。一些触发器具有时钟使能输入。当该输入未置位时，时钟被忽略。

## 门闩

锁存器名声不好，因为 FPGA 设计中一般不使用。至少，不是故意的。糟糕的编码会产生意外的闩锁，这会对 FPGA 工具造成严重破坏，尤其是当它们试图让电路以最快的时钟速度运行时。

然而，锁存器是一个重要的构建模块，它们非常容易理解。最简单的锁存器是 SR 锁存器(有时称为 SR 触发器)。S 代表置位，R 代表复位。如果您断言 S 输入，Q 输出也将断言。如果 R 输入置位，Q 输出不会置位。如果你断言 S 和 R 输入…不要这样做。结果未定义，这是使用 SR 锁存器的问题之一。

SR 锁存器的逻辑实现很简单。它是两个反相双输入门(NAND 或 NOR)交叉连接(见下文)。无论你选哪个门，你都要用它。如果使用与非门，S 和 R 输入将为低电平有效。如果你用一个或非门，它们会是高电平有效。Falstad 模拟器[有一个 NAND SR 锁存器](http://www.falstad.com/circuit/circuitjs.html?cct=$+1+0.000005+1.500424758475255+50+5+50%0A151+240+160+352+160+0+2+0%0A151+240+288+352+288+0+2+5%0Aw+352+160+352+192+0%0Aw+352+192+240+256+0%0Aw+352+288+352+256+0%0Aw+352+256+240+192+0%0Aw+240+192+240+176+0%0Aw+240+256+240+272+0%0AL+240+304+160+304+0+1+true+5+0%0AL+240+144+160+144+0+1+true+5+0%0AM+352+160+432+160+0+2.5%0AM+352+288+432+288+0+2.5%0Ax+143+120+174+123+0+24+set%0Ax+422+138+439+141+0+24+Q%0Ax+131+281+185+284+0+24+reset%0Ax+422+266+439+269+2+24+Q%0A)的示例电路，你可以从示例电路菜单中选择。

[![circ4](img/e1d2343adf0a798c6e32c466d0ccc134.png)](https://hackaday.com/wp-content/uploads/2015/09/circ4.png)

Verilog 中的很简单(如果你愿意，可以使用 nor):

```
module SR_latch(input R, input S, output Q, output Qbar); 
 nand (Qbar, R, Q); 
 nand(Q, S, Qbar); 
endmodule
```

然而，在 FPGA 上实际合成 SR 锁存器时，不应这样做。如果你的逻辑都是有时钟的，这些工具会做得更好。这只是一个构建模块，你可以用 Verilog 建模并不意味着你应该综合它。

## 下次

锁存器有其用途，尽管正如我前面提到的，在 FPGA 中使用锁存器会导致各种各样的时序问题。你真正想要的是带时钟的人字拖，这是下次的主题。

模拟的一个好处是，你可以很容易地进行实验，而不用担心让组件的魔力烟消云散。你能想出给 SR 锁存器增加一个使能输入的方法吗？也就是说，除非使能信号有效，否则锁存器会忽略 S 和 R 输入。有一种方法，这是我们下次要探讨的。

如果模拟让你渴望真正的硬件，你可以看看下面的视频。

 [https://www.youtube.com/embed/3sypB1YEFrM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3sypB1YEFrM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



你可能还想看看这个两部分系列的下一部分[。](http://hackaday.com/2015/09/24/learn-flip-flops-with-more-simulation/)