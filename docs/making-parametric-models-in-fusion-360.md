# 在 Fusion 360 中制作参数化模型

> 原文：<https://hackaday.com/2016/02/02/making-parametric-models-in-fusion-360/>

我们都知道并喜爱 [OpenSCAD](http://hackaday.com/2013/12/11/3d-printering-making-a-thing-with-openscad/) ,因为它有着甜美的参数。然而，Fusion 360 也有可能带来同样的好处。为了做到这一点，我们将为我们的对象建立一个数学模型，然后我们将改变变量以获得不同的几何形状。这比听起来简单。

即使您不使用 Fusion 360，了解不同设计工具的工作原理也很有好处。这是 Autodesk 生产的基于网络的 3D 建模软件。其中一个很好的特点是，它让我与其他人分享我的模型。我将在一分钟之内带你完成一个简单对象的建模。另一种描述我们将要学习的内容的方式是:在 Fusion 360 中建模时如何思考。

满足参数框。参数框包含模型中定义的每个维度(变量)。也可以添加自己的。这就是我们要做的，来制作参数模型。

![Parameters Box](img/5c066cb451e6c23feef63a24b114c45f.png)

Meet the parameters box.

![The parameters box is under modify in the modeling environment.](img/d3401e2ed5cea6d578ed1be53b0522db.png)

The parameters box is under modify in the modeling environment.

在本教程中，我们将制作一个盒子来存放小工具。我建议遵循 [Fusion360 模型](http://a360.co/1WIwTxb)中的步骤。Fusion360 窗口底部有一个带有回放控件的时间线。您可以前后移动滑块来查看不同的阶段。您也可以右键单击任何步骤，并选择“编辑草图”或“编辑特征”，以查看特定的内容。

在我开始制作盒子之前，我坐下来思考我该如何组装这个模型。因为它是参数化的，我知道我想要尽可能少的变量。我宁愿让计算机替我做这项工作。所以我想出了五件事来定义我的盒子。

1.  长度–盒子内部的长度。因为我的盒子是用来装东西的，所以我不在乎外面有多大。我宁愿让软件来计算。
2.  宽度–盒子内部的宽度。
3.  Height – The height of the inside of the box.![Your best friend. Secretly math.](img/66d4b424820c429588bcfaf621d868e0.png)

    你最好的朋友。秘密数学。

4.  厚度——墙壁和盖子的厚度。我也从这个数字中推导出顶部肋骨的厚度。
5.  配合–这是盖子和盒子之间的配合/间隙。0.25 毫米对于一台调谐良好的打印机来说相当容易。

接下来是素描。当使用任何现代 CAD 软件时，重要的是要记住，你所做的并不是真正的绘图，而是为你的对象建立一个数学模型。我倾向于认为这个过程是图形化编程。我看到很多新手犯的一个错误是完全忽略尺寸工具(快捷:D)和约束面板。这些约束告诉软件，从数学上讲，直线 A 总是平行于直线 B，或者圆 A 总是与直线 B 相切。掌握这一点可以让您创建模型，这些模型将随着尺寸和设计考虑的变化而扩展和调整。它也大大加快了你的起草时间。

关于草图的一些提示:

*   Fusion 有一些很棒的热键。我使用的一些工具有 Q-剪切/拉伸(推/拉)草图、D-尺寸、C-圆、L-线和 P-投影。
*   仔细检查你的约束。Fusion 对于它为您设置的约束是保守的。确保明显的在那里。
*   参数区分大小写。“厚度”并不等同于“厚度”
*   我可以画出盒子，然后使用盒子的关系，画出盖子。但是，如果草图中的形状不接触，它们将被挤出为单独的实体。

![A close up of the sketch used to generate this part.](img/3c5fec431ebbea9a7dd079bcb6f81e60.png)

A close up of the sketch used to generate this part. Note the fx: these are numbers taken from our parameters.

一旦零件轮廓完成，我选择盖子轮廓和盒子轮廓并挤压盒子。同样，因为我想在最后得到一个参数化的零件，所以在这个步骤中我没有输入数字，而是输入了我之前设置的变量。

 [![Here I say that I want the slide where the lid goes to be half the thickness of the wall. Later I'll set the distance between the lid and the edge of the slide to, "Fit."](img/1ccf431208882a84fc7930ca5f2c35f3.png "Draw with parameters")](https://hackaday.com/2016/02/02/making-parametric-models-in-fusion-360/draw-with-parameters-2/) Here I say that I want the slide where the lid goes to be half the thickness of the wall. Later I’ll set the distance between the lid and the edge of the slide to, “Fit.” [![When I extrude the part I set the length of the extrude to Length*2*Thickness. This is because when I add the sides I will be extruding into the part and will take up 1*Thickness one each side.](img/4a1850acbd19e0f063126de3304e2cc6.png "Extrude the thing")](https://hackaday.com/2016/02/02/making-parametric-models-in-fusion-360/extrude-the-thing/) When I extrude the part I set the length of the extrude to Length*2*Thickness. This is because when I add the sides I will be extruding into the part and will take up 1*Thickness one each side.

现在这个盒子是一个盖子和一个没有末端的挤压物。我需要把盒子的两端盖上。为此，我将使用一个平面和镜像操作来复制两端到两侧。如果那句话是错的，另一种方式认为这是伪代码。

> plane _ of _ symmetry = createmidplanbetween(boxend 1，boxend 2)；
> box _ end = cap box(end 1)；
> symmetricalCopy(box_end，plane _ of _ symmetry)；

一旦它开始意识到你不是在传统意义上绘制形状或建模，融合就开始变得更有意义了。你在用可视化的方式编程。顺便说一下，Fusion 中的镜像和图案命令非常酷，但是很复杂。如果这个功能给你带来了奇怪的结果(比如填满你盒子里所有的空白)，我会推荐你去看 YouTube 视频。

 [![plane_of_symmetry=createMidPlaneBetween(boxEnd1, boxEnd2);](img/c6860a3ceb6fd07bbef88d3c73d2b1a7.png "Make a da mid plane")](https://hackaday.com/2016/02/02/making-parametric-models-in-fusion-360/make-a-da-mid-plane/) plane_of_symmetry=createMidPlaneBetween(boxEnd1, boxEnd2); [![box_end=capBox(end1);](img/ca467e5297dc6f895e35335aaf493767.png "Extruda da other thing")](https://hackaday.com/2016/02/02/making-parametric-models-in-fusion-360/extruda-da-other-thing/) box_end=capBox(end1); [![symmetricalCopy(box_end, plane_of_symmetry);](img/4dc7b32edf4ab2af782d9d5c9ae3fb69.png "Mirror da thing")](https://hackaday.com/2016/02/02/making-parametric-models-in-fusion-360/mirror-da-thing/) symmetricalCopy(box_end, plane_of_symmetry);

下一步，我添加了一些装饰功能的盖子。这个![Make a da pattern](img/4934dcf36d23bbf9b05c5cff53193456.png)类似于前面的步骤:制作一个用变量标注尺寸的草图，然后用草图拉伸或切割。我用开槽工具在顶部添加了便于抓握的脊。在我添加了脊之后，我画了一个矩形，去掉了一些脊，这样我就可以有一个区域来写盒子里的东西。

现在是测试文件的时候了。我们将返回并打开参数窗口，更改其中一个尺寸。哦不！一个错误。像任何代码一样，它第一次没有编译成功。在这种情况下，当我绘制初始槽时，我没有将槽的中点约束到盖子的中间。我从盒子的一端到另一端画了一条线，确保将其两端约束到盖子的中间，然后使用重合约束将插槽的中间连接到这条线。建立数学关系。

![Oh no! An error in our code!](img/3ab8e14f354e0517cdf85e8f41c51cc2.png)

Oh no! An error in our code!

修好素描后，我又试了一次。有用！当我改变任何值时，我会得到一个新的盒子模型。正如你在这篇文章的开头看到的！我使用 make 命令为我的打印机生成 STL。然后，不可否认的是，在小盒子上有点过火了。

![Only a little overboard!](img/4944645db46aa650906b694f55fd8539.png)

Only a little overboard!