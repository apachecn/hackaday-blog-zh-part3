# Thingiverse 定制速成班

> 原文：<https://hackaday.com/2017/06/27/a-crash-course-in-thingiverse-customizer/>

OpenSCAD 是为 3D 打印(或其他目的)创建对象的一种很好的方式，尤其是如果您已经习惯于编程的话。对于像前面板这样的东西来说，它很棒，因为你可以很容易地进行修改，而且——如果你正确地编写了代码——一切都会自动调整到新的位置。

然而，如果您有一段通用的代码，并且您希望人们有能力定制它，该怎么办？例如，考虑以下代码:

```
$fn=100;
difference()
{
  cube([25,25,5]);
  translate([4,4,-1]) cylinder(h=7,r=2);
  translate([25-4,4,-1]) cylinder(h=7,r=2);
  translate([4,25-4,-1]) cylinder(h=7,r=2);
  translate([25-4,25-4,-1]) cylinder(h=7,r=2);
}
```

这就产生了你在右边看到的有四个钻孔的盘子。

## 习惯 101

显而易见，您可以使用变量，如果最终用户有 OpenSCAD 的副本，他们可以[更改东西](https://tinyurl.com/y8f4dlq8)(如果您想在浏览器中运行 OpenSCAD，请单击链接)而不用担心数学问题:

```
$fn=100;

w=25;   // size of square
thick=5;  // thickness
drillhole_r=2;  // radius of drill hole
drilloff=2;   // offset from edge of drill hole

difference()
{
  cube([w,w,thick]);
  translate([drilloff+drillhole_r,drilloff+drillhole_r,-1]) cylinder(h=thick+2,r=drillhole_r);
  translate([w-(drilloff+drillhole_r),drilloff+drillhole_r,-1]) cylinder(h=thick+2,r=drillhole_r);
  translate([drilloff+drillhole_r,w-(drilloff+drillhole_r),-1]) cylinder(h=thick+2,r=drillhole_r);
  translate([w-(drilloff+drillhole_r),w-(drilloff+drillhole_r),-1]) cylinder(h=thick+2,r=drillhole_r);
}
```

你可以很容易地改变顶部的变量，得到不同大小的盘子，而不必手动重新调整一切。如果您使用的是网页版，请按 F4 查看您的更改。对于本地副本，F5 可以做到。

## 不够好

不过，这还不够好。当然，像我们这样的人可以启动一个 OpenSCAD 副本并对程序进行修改，但这可能会让一些人感到困惑。然而，如果你把你的设计放在 Thingiverse 上(我会避开总会出现的政治问题)，你还有另一个选择。Thingiverse 提供了一个定制器选项，允许您构建一个简单的 GUI 来更改变量。这实际上与第一种情况相同，但是应用程序使用简单的注释来描述变量，并使用其他注释来设置选项。此外，变量必须由常量设置。

一般来说，如果打开 Customizer，每个设置为常量的变量都会显示在 GUI 中。我稍后将向您展示如何避免这种情况，但是现在，让我们插入这个简单的示例，看看它是如何工作的。由于没有特别的注释，您会得到这样的结果:

![](img/fd711e7231727fdddfd5be791d2e4c44.png)

这个其实[还不错](https://www.thingiverse.com/apps/customizer/run?thing_id=2350336)(需要 Thingiverse 登录)。每个变量(甚至$fn)都有一个文本框，您可以在其中键入不同的数字。变量名中的下划线变成了空格，每个空格都变成了大写。因此，即使是这样简单的设置也是可用的，尤其是如果您选择了好的变量名(可能我没有选择)。

不过，让它变得更好很容易。您可以在变量前的注释上添加描述性标题。例如:

```
// Width and height of plate (mm)

w=25;
```

这将为您提供一个更具描述性的名称。你也可以在变量后面加上注释来获得不同的效果。例如，这将为您提供一个滑块:

```
// Width and height of plate (mm)

w=25; // [10:100]
```

或者，您可以提供一个值列表:

```
// Bolt size (radius, mm)

drillholl_r=2; // [2,4,8,10]
```

如果您想要一种简单的方法来删除$fn 条目，您可以这样做:

```
$fn=100+0;
```

但是，还有更多高级功能可用。

## 先进的

[![](img/6ef903f1f174ab658a4b3ad60988f56f.png)](https://hackaday.com/wp-content/uploads/2017/05/part.png) 我不会介绍你可以用来上传图像或获得绘图画布的方法。你可以查看官方文件。然而，代码后面的[演示了一个更实际的设置。第一个注释定义了一个选项卡，您可以使用这些选项卡来组织变量集，以减少 GUI 的混乱。此外，您可以定义一个[Hidden]选项卡来隐藏您不想显示的变量。还有一个[全局]选项卡，无论其他选项卡显示什么，它总是可见的。](https://tinyurl.com/yac2mtaa)

否则，[示例](https://www.thingiverse.com/apps/customizer/run?thing_id=2349058)显示了基本的文本输入、滑块和带有一些额外特性的下拉菜单(例如，滑块上的步长)。你可以在左边看到结果。

```
/* [Main Dimensions] */
// Outside diameter (mm)
out_dia=50;
// Height (mm)
height=45;
// Cut diameter (mm)
cut_dia=30;

/* [Inner Dimensions] */
// Inner diameter (mm)
in_dia=21;
// Depth (mm)
in_depth=10; // [5,10,15,20,25]
/* [Options] */
// Line segments for circles (3 for triangles, 6 for hex, etc.)
FN=100; // [3:1:25]
// Override line segement count (any positive value)
OFN=0;

$fn=OFN?OFN:FN;

/* [Hidden] */
Num_copies=2;
// Num_copies=1+0; // stop customizer from picking this up

for (i=[1:Num_copies])
  translate([(i-1)*out_dia*3,0,0])
    difference()
    {
      union()
      {
      cylinder(center=false,r=out_dia/2, h=height);
      translate([-out_dia/2,-out_dia/2,height/2-height/8])
      cube([out_dia,out_dia,height/4]);
     }
  translate([0,0,-1])
  cylinder(center=false,r=cut_dia/2,h=1+height-in_depth);
  translate([0,0,,height-in_depth])
  cylinder(center=false,r=in_dia/2,h=1+in_depth);
  }
```

## 接下来……

我们一直很惊讶有人没有提出一个你可以在自己的网站上托管的独立版本。语法非常简单，我们打赌几行 Python 和 OpenSCAD 就能轻松完成。这将允许你在 Thingiverse 之外托管定制应用程序，并出售它们，或者让它们将完成的文件发送给服务机构。

我们发现我们很少再编写任何不支持 customizer 的 OpenSCAD 了。如果你做得对，几乎任何东西都是可重用的，有时重用的机会会令人惊讶。