# 如何用铝型材和 3D 打印支架制作任何东西

> 原文：<https://hackaday.com/2018/05/08/how-to-build-anything-out-of-aluminum-extrusion-and-3d-printed-brackets/>

3D 打印的真正威力在于零件的无限定制。当您将 3D 打印与现有材料相结合时，这变得尤为强大。我一直在开发一些简单的技巧，通过一两种你可能已经知道的技术，使通用紧固件和印刷连接器与铝挤压完美匹配。

用 3D 打印机工作足够长的时间，我们的想法不可避免地会超出我们的打印量。根据项目的性质，可以分成几部分，然后将它们粘在一起。但通常一个更大的项目也会对塑料提出更高的结构要求。

我们这些幸运地拥有不错的车间的人可以转向木工、焊接或金属加工来完成更大的项目。无论你有没有这种选择，铝挤压梁提供了我们需要的结构去更大，做得更快。此外，3D 打印还能让铝挤压变得更容易、更便宜。

## 一切都是由铝挤压而成

铝挤压梁对这些页面来说并不陌生。我们对它们有一个大概的了解，我们已经看到了很多使用挤压的项目，比如 T2 的卫星追踪器，T4 的魔方解算器，还有自动无人机充电站。许多流行的 3D 打印机都有铝挤压框架，因为它们比 3D 打印塑料提供更高的强度和更好的尺寸公差。

但连接器的选择很快扼杀了创造力，因为目录中的绝大多数连接器都是用于这种或那种 90 度接头的。成角度的连接器占少数，通常限于几个角度，如 30 度、45 度和 60 度。没有足够的销量来证明制造只有少数人会使用的角形连接器的合理性。这是我们的 3D 打印机重新进入画面的地方，作为低容量利基零件的工厂。

## 习俗并不意味着艰难

![](img/592c9287ec60dae58ea248ce2aac67a9.png)将定制与库存相结合，使我们能够利用每个部分的优势来设计项目:铝挤压提供通用结构，3D 打印塑料以特定于项目的方式将它们连接在一起。在(或[与拉链](https://hackaday.com/2015/11/03/print-your-own-vertices-for-quick-structural-skeletons/))之前，我们已经介绍过 [3D 打印直角连接器，但今天我们将重点介绍 3D 打印在非常精确地构建任意角度方面的优势。](https://hackaday.com/2017/12/16/if-3d-printer-then-custom-aluminum-extrusion-brackets/)

这些连接器的 CAD 设计非常简单。这通常是减去梁本身的矩形实体，然后减去几个圆柱体以创建紧固件的安装孔。对于 3D 打印塑料项目来说，三面螺栓连接挤压件(如这里的摇臂示例)通常足够坚固。这意味着我们可以经常跳过“顶”(相对于印刷床)面，以方便印刷。有时候，我们非常需要这种力量来处理桥接或其他一些技术，以给我们第四面，但我们现在将把这种挑战放在一边。关键是，你可以用最少的努力尝试一下，当你习惯了之后，就可以采用更多的技术。

## 一个例子:艰难的角度变得容易

我一直在设计一个摇臂子组件，它为这种讨论提供了一个完美的例子。这是我正在建造的机器人悬挂系统的一部分。整个设计太大了，无法打印成一个整体，所以我把这个物体分成由 3D 打印部件连接在一起的铝段。以下是线框图表:

[![Three-view of rocker arm with two aluminum extrusion beams adjacent to it.](img/958c7dff126272cc7ae3a0db76c13866.png)](https://hackaday.com/wp-content/uploads/2018/05/rocker-3view.png)

看看这两个挤压段的相对角度——没有挤压供应商会在这些角度上储存连接器，即使他们这样做，你也不会在它的中心得到一对轴承和顶部的机械连杆。这种特定于项目的细节使该中心成为一次性 3D 打印的理想选择。至于手臂，我们可以为两个长方形的塑料块进行 3D 打印。但是为什么呢？这里唯一与项目相关的细节是长度，它的切割速度远远快于打印相同长度的塑料，即使切割是用手锯完成的。

这篇文章的重点是在铝和塑料相遇的地方，所以我不打算深入到设置你的角度或移除挤压区域的细节。但值得注意的是，一些普通的 3D 打印行为强烈影响了这种构建技术。明智地选择您的层方向-当打印的零件被推到超出其极限时，它们通常会因沿层边界断裂而失败。沿每个轴至少使用两个紧固件，间隔大约与梁宽一样远，以分散工作负荷。仅仅使用一个紧固件就把这个单点变成了一个支点，使我们打印的零件上的力倍增，这是我们不希望的。

 [![Bridge Assist CAD](img/450111dee4641da7cb352fd6a127b761.png "Bridge Assist CAD")](https://hackaday.com/2018/05/08/how-to-build-anything-out-of-aluminum-extrusion-and-3d-printed-brackets/bridge-assist-cad/)  [![Bridge Assist printed](img/2f4e0a7ecbc32808be86f8074f2f9d69.png "Bridge Assist printed")](https://hackaday.com/2018/05/08/how-to-build-anything-out-of-aluminum-extrusion-and-3d-printed-brackets/bridge-assist-printed/)  [![Rocker Arm 16x9](img/f2de70b8e9d5de3cd207ae01f922ba8e.png "Rocker Arm 16x9")](https://hackaday.com/2018/05/08/how-to-build-anything-out-of-aluminum-extrusion-and-3d-printed-brackets/rocker-arm-16x9/) 

还有一点要考虑的是，当螺栓孔没有很好地与印刷床对齐时，会出现突出。我们可以帮助我们的打印机桥接奇怪的螺栓头表面，方法是创建一个薄层(2-3 个打印层高度厚)覆盖螺栓孔，在达到目的后可以用钻头清理。这些比印刷支架的典型解决方案更容易移除并且消耗更少的材料。

## 秘方:T 型槽插件、T 型螺母、T 型管的替代品

一旦我们有了一个项目定制的连接器设计和印刷，我们继续组装，在那里我们面对铝型材的另一个隐藏的陷阱:特种紧固件。称为 T 型槽插件，T 型螺母，或一些类似的名字，他们的形状特别适合铝挤压梁的插槽。它们也非常昂贵。不一定是绝对意义上的，但肯定是相对于类似尺寸的商品六角螺母。我们的摇臂示例是为 15 毫米 [Misumi 3 系列](https://us.misumi-ec.com/vona2/detail/110300465870/)挤压件设计的。Misumi 为这种挤压提供了几种特殊的坚果，最便宜的“经济”型号[售价 8.28 美元一袋 100 个。相比之下，我们值得信赖的硬件供应商 McMaster-Carr 以 0.88 美元一袋 100 个的价格提供通用 M3 六角螺母。(](https://us.misumi-ec.com/vona2/detail/110300465710/)[目录号 90592A085](https://www.mcmaster.com/#90592A085) )

[![](img/a50baadacbe7f68989cf029378d9e5f9.png)](https://hackaday.com/wp-content/uploads/2018/05/misumi3vs5.jpg)

15mm Misumi 3 Series (right) is friendlier to using generic M3 hex nut (shown) than its 20mm sibling 5 Series (left) shown with matching specialty fastener.

在我们屈服于 90%折扣的诱惑之前，让我们快速回顾一下使用普通坚果的好处。第一个也是最明显的障碍是特定挤压梁的轮廓可能不允许使用普通螺母。第二，普通螺母与槽内表面的接合程度不同于为挤压型材定制的螺母。这通常意味着我们不能在某些东西滑动之前将螺栓拧紧。第三，高端特种螺母通过其形状、尺寸或额外的薄金属弹簧将螺母固定在适当的位置，提供抵抗挤压的摩擦力。螺母留在原位，而不是在槽中滑动，这简化了组装，减少了时间浪费，降低了组装者的挫折感。这样节省的劳动力可以超过专业紧固件的成本。

对于这个摇臂的例子，第一个问题并不适用，因为 Misumi 3 系列是宽容的通用 M3 螺母。第二项——降低紧固件扭矩限制——是可以接受的，只要它仍然足以满足我们对 3D 打印塑料项目的需求。第三项——组装的便利性——是我们可以通过一些巧妙的 3D 打印来获得的。

我们现在将 3D 打印的优势(一个小批量、特定任务对象的工厂)应用于铝挤压梁中的通用紧固件。我们的技术使用了一个专门为这项工作设计的小工具。对于初学者来说，这个工具有一个小驼峰，作为一个弹簧，有助于保持其在插槽中的位置。然后，因为工具是沿着它将被使用的零件设计的，我们可以设计它的托盘来容纳普通的螺母，其间距正好是我们需要的距离。作为锦上添花，我们在末尾加了一个小钩。这个钩子——设计成当 hub 在手臂上就位时露出来——允许我们微调我们的位置，而不必拆开东西。

[![](img/95764c80867d96dd641cee4a6cc899c5.png)](https://hackaday.com/wp-content/uploads/2018/05/insert-isometric.png)

为了适应插槽中留下的狭窄空间，该工具被打印得尽可能薄:我们 3D 打印机喷嘴的宽度。这也使得细丝的使用更加经济，并且打印速度非常快，这两个属性对于一次性物品都很有用，因为一旦拧紧螺栓，这种薄定位工具就不能被移除。不过，这种牺牲是值得的，因为它将令人沮丧的对齐小紧固件的工作变成了一件极其简单的任务。

 [![Insertion Tool With Associated Parts](img/dbe7bb185a9e9ab969118a0aaa2576ca.png "Insertion Tool With Associated Parts")](https://hackaday.com/2018/05/08/how-to-build-anything-out-of-aluminum-extrusion-and-3d-printed-brackets/rocker-arm-2-insert-tool/)  [![Partially Inserted Tool](img/752fb2714853eab344ef5e799fadd1ed.png "Partially Inserted Tool")](https://hackaday.com/2018/05/08/how-to-build-anything-out-of-aluminum-extrusion-and-3d-printed-brackets/rocker-arm-3-half-installed/)  [![Insertion Tool In Place](img/5b90e4b38f855955035f40a682f6ae6b.png "Insertion Tool In Place")](https://hackaday.com/2018/05/08/how-to-build-anything-out-of-aluminum-extrusion-and-3d-printed-brackets/rocker-arm-4-fully-inserted/)  [![Installation Complete](img/4779b09453053c47fd3e3c3b7d452559.png "Installation Complete")](https://hackaday.com/2018/05/08/how-to-build-anything-out-of-aluminum-extrusion-and-3d-printed-brackets/rocker-arm-5-bolts-installed/) 

试试这种紧固件方法。我希望你会发现这项技术很有用，我期待看到更多的项目将 3D 打印和铝挤压梁的优势结合到一起，而这两者都无法单独完成。如果你对你的结果感到自豪，不要羞于通过我们的[提示热线](https://hackaday.com/submit-a-tip/)告诉我们，或者作为我们的 [Hackday 奖](https://hackaday.io/prize)的参赛资格。快乐大厦！