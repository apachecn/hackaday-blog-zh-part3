# 拆卸:AH-64A 阿帕奇数据输入面板

> 原文：<https://hackaday.com/2018/04/30/milspec-teardown-ah-64a-apache-data-entry-panel/>

是时候再一次看看这些税收是怎么花的了，这次是以休斯直升机公司制造的“数据输入键盘”的形式。这个装置大约建于 1986 年左右，用于 AH-64A 阿帕奇。具体来说，这个面板应该位于炮手的左膝，作为阿帕奇火控系统的通用输入设备。最终阿帕奇升级为所谓的“玻璃驾驶舱”；将各种车辆功能整合到少数多用途数字显示器中。因此，这种特殊的设备变得过时，并从现役阿帕奇机队撤出。

[![](img/4c26232c50c1f9a75074894621829000.png)](https://hackaday.com/wp-content/uploads/2018/04/datakbd_plate1.png) 外面的军车爱好者可能知道，虽然阿帕奇目前是波音公司的产品，但它最初是由休斯直升机公司设计的。1984 年，麦道公司购买了休斯直升机公司并接管了阿帕奇的生产，然后麦道公司在 1997 年与波音公司合并。

因此，这是有点意思的是，这种设备的名称为休斯直升机，因为当时它是制造，他们将被称为麦道直升机系统。据推测，他们不得不处理现有库存的部件，这些部件已经打上了休斯的商标，留下了一些过渡性的例子，比如这个例子。

但你不是来这里上美国军事工业综合体的历史课的，你想了解硬件本身。所以让我们打开它，看看我们能从这段航空史中学到什么。

## 尽职调查:这是什么东西？

[![](img/f63f95c2b5fdfca896b724ede879a1cc.png)](https://hackaday.com/wp-content/uploads/2018/04/datakbd_cockpit1.jpg)

Credit: Robert Francis [via YouTube](https://www.youtube.com/watch?v=csiZ0nhuBvQ)

我应该提到的是，当我第一次得到这个特殊的作品时，我不知道它是什么。像我的大多数其他军事发现一样，这个出现在我为剩余电子元件设置的易贝警报中，并被简单地列为“军事剩余数据输入键盘”。它看起来有点破旧，但很便宜，我喜欢便宜。

当它到达时，仔细一看发现了印在设备背面铭牌上的合同号，在网上搜索使我扫描了 1988 年的技术公告 55-1520-238-23-1，“直升机，攻击 AH-64A 的保修计划”。果然，在附录 A“AH-64 保修部件”中，列出了“面板组件，数据输入 K/B O”。所以现在我知道这个特殊的硬件是来自最初的 AH-64A 阿帕奇。不幸的是，最后一架 AH-64A 在 2012 年被改装成 AH-64D，所以找到驾驶舱的照片比我预期的要困难一些。

最终，YouTube 化险为夷。我发现有人上传了他们坐在 2010 年仅存的 AH-64A 阿帕奇上的视频，果然你可以看到他在面板上移动时的“数据输入键盘”。谜团解开了。

## 键盘解剖

从键盘本身开始拆卸似乎是合理的，键盘用六个螺栓固定在设备的前面。卸下螺栓后，您就可以拉开键盘，取出固定背板的小螺钉。

[![](img/36ff729392e36ec9f75c84dd5b2e4e3e.png)](https://hackaday.com/wp-content/uploads/2018/04/datakbd_kbd.jpg)

随着键盘被分解为基本组件，我们可以看到其操作与我们习惯使用的廉价薄膜键盘并没有太大的不同。这里的机制当然更加健壮，因为它是为军用飞机设计的，但想法是一样的。设备正面的每个按键都会推动一个小薄膜圆顶，进而与 PCB 上的走线接触。然而，每个圆顶上都有金属触点，还有一个微小的弹簧，所以按键上的触觉反馈非常好。当您的操作员戴着手套并可能处于战斗状态时，这一点非常重要。

 [![datakbd_kbd1](img/e01baef561312483f02422bb1083f9a7.png "datakbd_kbd1")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/04/datakbd_kbd1.jpg?ssl=1)  [![This is from an attack helicopter.](img/c5703c558b1ce15d9c3e413333fd3b2d.png "datakbd_kbd2")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/04/datakbd_kbd2.jpg?ssl=1) This is from an attack helicopter. [![datakbd_kbd3](img/0aef383bb96ccdf47c05ee2ff0a6565e.png "datakbd_kbd3")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/04/datakbd_kbd3.jpg?ssl=1) 

## 内部结构

随着键盘本身的拆除，我们第一次看到了设备的内部。我立刻就被贯穿始终的绝对华丽，无疑也是极其昂贵的连接器所震撼。大概是为了防止振动损失，连接器不能简单地拔出来，你需要一个小平头螺丝刀来拧开并分离它们。它们被设计成只能以一种方式连接在一起，并防止针脚弯曲，因为你别无选择，只能均匀地松开或拧紧两侧，否则它会被卡住。毫无疑问，他们很难相处，但是你不得不佩服他们。

 [![datakbd_con1](img/64f7cc355167c1411c64ec2057065ab6.png "datakbd_con1")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/04/datakbd_con1.jpg?ssl=1)  [![datakbd_con2](img/7c947679b7150bbc0d07535facee8209.png "datakbd_con2")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/04/datakbd_con2.jpg?ssl=1) 

令我惊讶的第二件事是，该设备内部实际上有两个独立的电路板，通过背板连接在一起。背板具有一个标准的 DB15 插头端口，顺便说一下，这是整个设备上唯一的外部电气连接形式，通过更大版本的拧紧连接器连接到“刀片”。

[![](img/75b575ab76d9136b3bea1ce2e32b143a.png)](https://hackaday.com/wp-content/uploads/2018/04/datakbd_backplane.jpg)

## 电源

我们要看的第一个“刀片”是电源。这块板特别简单，事实上它看起来几乎是自制的。电路板上的痕迹看起来像是用记号笔掩盖起来的，元件少到了极点。这里展示的明星是德州仪器公司的 LM123K，这是一款军用级 5V 稳压器，可提供高达 3A 的电流，并可处理高达 20V 的输入电压。有一个电感和一些电容来帮助平滑，但仅此而已。

 [![datakbd_psu](img/8165c6bc1b3f4c3512355dcf2e92615c.png "datakbd_psu")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/04/datakbd_psu.jpg?ssl=1)  [![datakbd_psuclose](img/0a0289cb8b0cddd4b3cb9f6d2b4ff796.png "datakbd_psuclose")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/04/datakbd_psuclose.jpg?ssl=1)  [![datakbd_psuback](img/d302cf253def2ef4186e33c6502fe5ce.png "datakbd_psuback")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/04/datakbd_psuback.jpg?ssl=1) 

我觉得它很有趣，这个设备有自己强大的内部电压调节器。这种东西似乎可以安装在一个单独的模块中，为驾驶舱中的所有设备提供 5V 电压。也许从可靠性的角度来看，设计人员认为最好为每个关键任务设备提供专用电源。

## 计算台

现在我想象在这个设备里会有一些有趣的电子设备，这就是我买这个东西的全部原因。但没想到里面会有一台完整的*电脑*。

 [![datakbd_cpu1](img/7ccc4faf6b9fd8d2cbeba3dcd430f2aa.png "datakbd_cpu1")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/04/datakbd_cpu1.jpg?ssl=1)  [![datakbd_cpu3](img/8863338ab789fdc5887cd75f19e64ff5.png "datakbd_cpu3")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/04/datakbd_cpu3.jpg?ssl=1)  [![datakbd_cpu2](img/45d9179245b44238604456ae7b9a39b1.png "datakbd_cpu2")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/04/datakbd_cpu2.jpg?ssl=1) 

“数据输入键盘”由一个[英特尔 MD8085AH/B](http://www.cpu-world.com/CPUs/8085/Intel-MD8085AH-B.html) 驱动，这是古老的英特尔 8085 CPU 的军用版本，与一个 MD8155H/B 2048 位 HMOS RAM 模块配对。ROM 存储在双 MD 8755 a/B 2 KB eprom 上。根据各自的数据表，所有这些组件都被评为“V 级空间级别”，因此，如果你计划建造火星漫游车或其他东西，这可能是一些非常昂贵的芯片的良好来源。

## 启动电源

在本系列的上一期中[，我成功地复活了一台 70 岁的“CP-142 系列计算机”](http://hackaday.com/2018/02/19/milspec-teardown-cp-142-range-computer/)，所以我觉得有义务在这台相当不陈旧的设备上尝试一次类似的壮举。我被设备上的标准 DB15 连接器以及它很容易找到电源引脚的事实所激励；我所要做的就是检查 LM123K 调节器的输入引脚和连接器引脚之间的导通性。从数据手册中了解到调节器可以处理高达 20V 的电压，我在连接器的相应引脚上提供了 12V 的“数据输入键盘”,并希望一切顺利。

[![](img/9c0cf7cb181c6f57fe5cb42b136ba2ce.png)](https://hackaday.com/wp-content/uploads/2018/04/datakbd_signal1.jpg) 我用示波器在剩余的引脚周围探测，希望看到数字通信的蛛丝马迹。最终我找到了*的东西*，但看起来要么是我对这个设备应该如何工作做出了天真的假设(很有可能)，要么是它有问题。确实有某种数字信号从设备中发出，当我按下不同的键或旋转旋钮时，信号会发生变化，但信号非常微弱，非常混乱。

只有大约 150 毫伏，并被某种背景噪音所掩盖，这并没有让我觉得是意料中的行为。我的感觉是板上有什么东西坏了，但是我做的两次检查(CPU 得到正确的电压，时钟处于正确的频率)没有显示任何明显的错误。虽然有这么旧的硬件，它可能是隐藏在电路板某处的坏电容。看看是否有任何 Hackaday 读者可能以前使用过这种硬件，并可能对我所看到的有所启发，这将是一件有趣的事情。

## 最后的想法

我没想到会这样，但这个设备实际上是由有用和有价值的组件组成的。键盘本身可以很容易地与安全系统或类似项目连接，并成为一个[令人敬畏的 PIN pad。有多少人可以说他们使用 Apache 中的真实硬件来处理身份验证？](https://hackaday.com/2013/09/05/custom-car-keypad-entry/)

计算机本身，如果你对那种东西感兴趣的话，是一个不可思议的发现。虽然年代久远，但这些军用级计算机部件非常有价值，可能会成为一个极其独特的逆向计算机的组成部分。丢弃现有的 ROM 将是有趣的第一步，而[用 UV](https://hackaday.com/2018/01/17/improvising-an-eprom-eraser/) 清除芯片并用新代码替换 ROM 是下一个合乎逻辑的步骤。

总的来说，我认为这是整个军事技术的一个奇妙的缩影。建造这个设备的成本肯定是天文数字，但是一旦你看了里面的东西，你就不能否认这个建筑在当时是非常昂贵的。几年后，当 Apache 更新时，所有的钱和 R&D 都被扔进了这个不起眼的键盘。不管建造一件东西要花多少钱，你都不能阻止前进的步伐。