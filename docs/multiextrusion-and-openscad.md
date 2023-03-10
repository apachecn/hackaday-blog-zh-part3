# 多重挤压 3D 打印和 OpenSCAD

> 原文：<https://hackaday.com/2017/01/20/multiextrusion-and-openscad/>

在最近一篇名为 [*骗子的 3D 打印*](http://hackaday.com/2016/12/27/liars-3d-printing-multiple-colors-with-one-extruder/) 的帖子中，我向你展示了即使你的打印机只有一个挤出机和热端，你也可以用多种灯丝颜色打印。然而，这并不容易，你在 Thingiverse 等网站上找到的许多模型都太复杂了，无法给出好的结果。一个有 800 层，每层都有两种颜色的物体会有很多灯丝变化，只有我们当中最有耐心的人才能忍受。

这意味着你可能想要制作自己的模型。问题是，怎么做？答案当然是很多不同的方式。我将讲述我是如何使用 OpenSCAD(见下文)制作上一次展示的两个模型。该软件实际上非常适合这个黑客，让我很容易地创建几个模型的框架来代表不同的颜色。

 [![dot](img/10e1078701975732f8af89b9470b8d0f.png "dot")](https://hackaday.com/2016/12/27/liars-3d-printing-multiple-colors-with-one-extruder/dot/)  [![wd5gnrsm](img/46ad47f84ba59d4f00ecabccbf1e692a.png "wd5gnrsm")](https://hackaday.com/2016/12/27/liars-3d-printing-multiple-colors-with-one-extruder/wd5gnrsm/) 

## 关于 OpenSCAD

关于 OpenSCAD 我就不多说了。与其说它是一个 CAD 软件包，不如说它是一种让你创建形状的编程语言。我们在之前已经[报道过它，尽管它会不时改变，所以你最好还是去读一下](http://hackaday.com/2013/12/11/3d-printering-making-a-thing-with-openscad/)[的官方手册](http://www.openscad.org/documentation.html)。

然而，总的想法是使用模块来创建原语。您可以旋转和平移它们(即移动它们)。也可以加入他们(union)，取他们的差(difference)。最后一点尤其重要。例如，看看上面的呼号牌。暂时忘了这篇课文。看到这两个洞了吗？下面是创建该形状的 OpenSCAD:

```
 difference() {
 cube([basew,basel,basez]);
 // cut holes
 translate([4,basel/2,0]) cylinder(r=2,h=basez+2);
 translate([basew-4,basel/2,0]) cylinder(r=2,h= basez+2);
 }
```

立方体“调用”创建基础。圆柱体是孔，区别“调用”是什么使它们成为孔而不是实心圆柱体(首先是实心的，之后的一切都被拿走)。一个关键点:整件事用的(主要)是变量，而不是数字。这意味着如果你改变了某个东西的大小，如果你写好了脚本，一切都会相应地调整。让我们看看如何将这些技术应用于多种颜色。

## 两种颜色

要驱动一台有两台挤压机的打印机(或者你谎称有一台)，你需要生成两个不同的 STL 文件，每台挤压机一个。这意味着很有可能其中一个只是“漂浮”在空中，这没关系，因为在现实中，它下面会有另一种颜色。

有很多方法可以做到这一点。我做了一个简化的假设:你的对象将主要是一种颜色，然后你将有一种或多种颜色作为对象的一部分。然后我写了一个由几个 OpenSCAD 模块组成的简单框架。

在 OpenSCAD 中，您认为是函数的东西被称为模块。在这个框架中有三个模块你需要考虑:object_1、object_2 和 object_3。本质上，您将 OpenSCAD 代码放在那些引用您想要的每种颜色的模块中。下面是测试框的代码(我让 object_3 为空):

```
module object_1() // first object, main color
{
 cube([basew,basel,basez]);
}

module object_2() // 2nd objects
{
 translate([basew/2,basel/2-5*dotr,basez-dothi/2])
   cylinder(r=dotr,h=dothi,center=true);
 translate([basew/2,basel/2+5*dotr,basez-dothi/2])
   cylinder(r=dotr,h=dothi,center=true);
 translate([basew/2,basel/2,basez/2])
   rotate([0,90,0]) cylinder(r=dotr,h=basel,center=true);
}
```

前两个圆柱是顶点。他们只是翻译到正确的位置。第三个圆柱体旋转并出现在盒子的中间。请记住，每一层有一个彩色点将采取灯丝变化。如果你真的有两个挤出机，这不是问题，但如果你在撒谎，每次工具更换都是一些手工工作，因为你暂停并手动交换单个头上的颜色。

## 获取 STL

为了让事情正常运行，您还需要改变一件事情。在框架文件的底部，有一些行大部分被注释掉了:

```
// ********************************
// To generate, pick one of these and render (F6)
// then if you picked one of the create_* you can
// export to STL. No need to export the preview
//preview_obj();
create_obj1();
//create_obj2();
//create_obj3();
```

在任何给定时间，这些行中只有一行应该取消注释。进行设计时，不要注释 preview_obj。这将让你看到整个物体的每一块都有不同的颜色。

当您准备好创建 STL 文件时，注释掉预览行并取消其中一个创建行的注释。然后使用 F6 渲染(完全渲染)。完成后，导出 STL 文件，然后替换该行的注释，并取消下一行的注释。然后重复 F6 渲染和导出。在这种情况下，你不必做对象 3，因为里面什么也没有。

## 会发生什么？

框架的其余部分非常简单。当你在对象 1 上创建时，它会绘制你的对象并减去所有应该是另一种颜色的地方。另外两个 create 调用只是呈现您指定的对象。我假设颜色 2 和颜色 3 不会有任何部分相交。如果你这样做了，你必须做一些更复杂的事情(也就是说，从第二个对象中减去第三个对象；也不会那么难)。

就是这样。如果您可以在 OpenSCAD 中建模，您可以创建多个拉伸模型。如果你撒谎，你可以用一台挤压式打印机打印出来，就像我一样。我没有试过，但是你应该可以用第二种颜色来切掉突出部分，用第三种颜色来建造定制的支撑结构。然后，您只需不导出第二种颜色，继续进行正常的双色打印。

显然，这不是唯一的方法。事实上，在 OpenSCAD 中这甚至不是唯一的方法。但这是一种制作简单多色模型的简便方法，适合与骗子的印刷方法一起使用。如果你不想安装 OpenSCAD，你可以试试你的浏览器，或者你可以用 T2 的 OpenJSCAD 做类似的事情。