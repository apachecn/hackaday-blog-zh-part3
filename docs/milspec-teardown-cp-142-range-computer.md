# Milspec 拆卸:CP-142 系列计算机

> 原文：<https://hackaday.com/2018/02/19/milspec-teardown-cp-142-range-computer/>

正如我之前在 Hackaday 的一些工作可以证明的那样，[我是二战技术的狂热粉丝](http://hackaday.com/2017/12/21/retrotechtacular-field-assembly-of-the-p-47/)。乘坐木制飞机进入太空，乘坐喷气式战斗机和[太空火箭](http://hackaday.com/2017/11/03/books-you-should-read-v-2-by-walter-dornberger/)离开太空，这一直吸引着我。因此，当我精心制作的易贝警报被一个自称是“海军二战靶场计算机”的东西触发时，可以肯定地说，我对此很感兴趣。

提醒你一下，我不是说我知道那是什么东西。我只知道它看起来很旧，我必须拥有它。当我急切地等待这款设备送到我家门口时，我试着对它做了一些研究，结果几乎一无所获。正如你可能想象的那样，许多 20 世纪 40 年代开发的硬件技术信息还没有进入互联网。有人在另一个网站上以 100 美元的价格出售一本可能涵盖该设备功能的技术手册，但我认为这可能有点过分。另外，这有什么意思呢？

我决定通过仔细检查硬件，查阅我能从它的单个组件和一些现代设备上获取的少量技术数据，来尝试破译这个设备的功能。最后，我想我对它是如何工作的有了一个很好的想法，但我当然很想知道是否有任何人实际上可能使用过这样的硬件，并且可以填补任何空白。

## 概观

我首先被这个东西的巨大和沉重所震撼。与现代硬件相比，CP-142 就像一辆真正的坦克。它由厚厚的折叠金属板制成，带有某种迷人的褶皱涂层，看起来就像是“老派军队”。它的大小和形状大致相当于一个工具箱，底部有一个开口，这让我觉得它原本是用来跨在其他硬件上的。

控制非常简单:左边有一个电源开关和“强度”转盘，右边有一个观察机械读数的窗口，上面写着“英里”。在这个装置的侧面有一个 70 毫米的刻度盘，当它旋转时可以移动计数器。很明显，旋转转盘是为了设定一个特定的距离，但稍后会详细说明。

 [![cp142_pwr](img/a58d803ba73004495a4d85c880b614d1.png "cp142_pwr")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/02/cp142_pwr.jpg?ssl=1)  [![cp142_miles](img/527c3a47057bf3b4011aa0105c6e85f5.png "cp142_miles")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/02/cp142_miles.jpg?ssl=1)  [![cp142_dial](img/57231ad36c678514121ddba19c52c0b4.png "cp142_dial")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/02/cp142_dial.jpg?ssl=1) 

松开底部的两个指旋螺钉后，CP-142 可以在铰链上打开，以查看内部组件。靠近主控制器的两个清晰标注的微调旋钮似乎表明，打开硬件摆弄内部部件并不罕见。甚至还有一个小六角键连接到设备的框架上，可以用来松开或移除控制转盘，这样操作者就可以将标记的刻度与外壳前面的指针对齐。

## 电子部分

CP-142 的左侧专用于电子设备，包括四个 12UA7 电子管、一个 6AK5、一个 6AL5 和一个雷神 UX-7350 变压器。这个设备中没有 PCB，所有的布线都是点对点进行的，只有几个硬金属“轨道”。

 [![cp142_elec](img/b32db1afeb8f71e9ff7049e7d37a9ee7.png "cp142_elec")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/02/cp142_elec.jpg?ssl=1)  [![cp142_wiring2](img/ce58601af85bb3582a4416b6fc25af4d.png "cp142_wiring2")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/02/cp142_wiring2.jpg?ssl=1)  [![cp142_wiring1](img/e4ec44aa3eef8500771a5bc5a31869d3.png "cp142_wiring1")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/02/cp142_wiring1.jpg?ssl=1) 

## 接线

一束厚厚的电线从电子部分出来，进入位于盖子铰链正下方的汇流条。这里还有一个开关，当盖子打开时，它会切断设备的电源。很明显，该装置将被打开到足够大的程度，因此有必要采用安全联锁装置和方法来防止电线因反复打开和关闭而疲劳。

这捆电线每隔 10 毫米左右用黑线缠绕一圈，这肯定是手工完成的。感觉与当时制造业劳动力的联系是不可思议的。十有八九，一个站出来支持战争努力的女性劳动力的任务是将这些小线环绑在电线束上，每天八个小时，与这些工人一起布线和进行点对点焊接。

在汇流条上方，电线连接到电源开关、亮度刻度盘和点亮机械显示器的灯泡。开关的结构是我以前从未见过的，它不是你通常期望的那个时代的胶木机身(CP-142 的其他区域也有)，而是由某种纤维板的夹层制成。

 [![cp142_bar1](img/da758e02e9bfdc6b9fb49642b098f4ca.png "cp142_bar1")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/02/cp142_bar1.jpg?ssl=1)  [![cp142_bar2](img/f8b5f0918b4141bacfc37ef7cc0be273.png "cp142_bar2")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/02/cp142_bar2.jpg?ssl=1)  [![cp142_rearcontrol](img/45f3ba80104f0378cdf5a8ffd3a7ec6d.png "cp142_rearcontrol")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/02/cp142_rearcontrol.jpg?ssl=1) 

## 刻度盘组件

CP-142 中的一切都是对 70 多年前硬件，尤其是军事硬件是如何设计的精彩展示。但在这台机器的所有部件中，表盘组件是最令人印象深刻的。它接受用户的输入，但也为他们提供当前所选范围的实时显示。这是机械完成的，计数器和刻度盘在同一根轴上。

一对锥齿轮被用来连接轴和一个巨大的电位计，电位计与刻度盘成 90 度角安装。旋转终点挡板由一小段螺杆和骑在螺杆上的一个小约束螺母提供。螺母不能转动，所以当刻度盘转动时，它在杆上水平移动。一旦它达到最小或最大行程，精密加工的壁架开始接触，使进一步的旋转不可能。

 [![cp142_dial1](img/e1c09f3dd8ef7da852673b2ede6aaada.png "cp142_dial1")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/02/cp142_dial1.jpg?ssl=1)  [![cp142_dial2](img/50257c5babd387926345938a126268b1.png "cp142_dial2")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/02/cp142_dial2.jpg?ssl=1)  [![cp142_dial3](img/df27d929b6e8b2513481b136d95220ed.png "cp142_dial3")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/02/cp142_dial3.jpg?ssl=1)  [![cp142_dial4](img/2b86192b63f0623f32453c38053998e4.png "cp142_dial4")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/02/cp142_dial4.jpg?ssl=1)  [![cp142_pot](img/219ea17ddf4f4d8ee36ff5edb7778411.png "cp142_pot")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/02/cp142_pot.jpg?ssl=1) 

对于你的输入设备爱好者来说，我不得不说，这个转盘上的动作是*难以置信的*。表盘本身重 260 克，即使包含所有机械运动，手感也极其光滑。在过去的几天里，我花了太多的时间来来回回地转动这个刻度盘。

## 唤醒沉睡的巨人

我不确定从什么时候开始我决定尝试启动 CP-142。我不停地看着贴在设备上的红色标签，上面写着“测试合格——4/6/54 ”,想知道一台存放了 64 年的机器是否还能工作。

没有一根电线被贴上标签，但真空管的文件很容易获得([12au 7 仍然被用于音频放大器中](https://hackaday.com/2016/06/19/simple-vacuum-tube-preamp-results-in-a-beautiful-build/))，用一个万用表我可以跟踪一切的走向。汇流条和精心设计的彩色电线也帮了大忙。我知道真空管需要什么样的电压，以及它们应该在哪个管脚上得到。从理论上讲，这应该只是将正确的电压插入母线，并期待最好的结果。

 [![cp142_powered](img/db81c1e2b26afb4d8cb4afdbacc0925e.png "cp142_powered")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/02/cp142_powered.jpg?ssl=1)  [![cp142_powered2](img/32567c5074d02bcee524b61ef14d6d3a.png "cp142_powered2")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/02/cp142_powered2.jpg?ssl=1)  [![cp142_powered3](img/eb7bcd4f2af3611ac595bcc32be1c9f2.png "cp142_powered3")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/02/cp142_powered3.jpg?ssl=1) 

老实说，当我看到显示器闪烁，那些电子管开始预热，这是六十多年来的第一次，对我来说这是一个非常不可思议的时刻。这是我一直钦佩的技术，但让这段合法的历史在我的工作台上运行给了我一个与那个时代联系的机会，这是我以前从未有过的。

## 操作理论

由于我对“计算机”这个词的现代解释，我最初认为这个设备会从雷达上获取某种信号，并使用它来旋转物理计数器。但是当我把它拆开时，我意识到计数器连接着一个电位计，电位计的值是由车载电子设备读取的。从逻辑上讲，似乎电子设备必须采用电位计的可变电阻，并将其转换为真空管正在放大的频率。

在底部有两个 N 型射频连接器，我认为如果我把示波器放在它们上面，我应该能够看到在我操纵控制装置时发生的事情。其中一个连接器似乎没有任何有趣的事情发生，但在第二个连接器上，我看到了我正在寻找的确认信息:

 [![Baseline signal](img/728cfa65cdd8f0a3249ae6014470466e.png "cp142_baseline")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/02/cp142_baseline.jpg?ssl=1) Baseline signal [![After adjusting controls](img/4d3b717004c3b3eede52dadd90e90a29.png "cp142_active")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/02/cp142_active.jpg?ssl=1) After adjusting controls

## 最后的想法

看到示波器在我旋转 CP-142 上的转盘后活跃起来，我相信，虽然我可能不会对这个特殊的老式战时技术 100%正确，但我肯定很接近了。当然，还有一些问题。雷达如何处理这个信号？第二个射频连接器有什么作用？

无论如何，我对自己获得的关于 CP-142 的知识数量感到满意。通常在拆卸的这个时候，我会开始考虑如何从设备中回收零件，但在这种情况下，这似乎不太合适。即使这个拨号盘组件只是一个 Arduino，离成为一个*令人敬畏的* USB 输入设备还有一段距离，这个老手将在我办公室的架子上享受它退休的剩余时光。我们一起上历史课。