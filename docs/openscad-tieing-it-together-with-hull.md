# OpenSCAD:将它与 Hull()绑定在一起

> 原文：<https://hackaday.com/2018/02/13/openscad-tieing-it-together-with-hull/>

你最喜欢的 [OpenSCAD 命令](https://en.wikibooks.org/wiki/OpenSCAD_User_Manual)是什么？也许是`intersection()`或者`difference()`？或者你是一个`polygon()`和`extrude()`的建模者？对我来说，最有用的，也可能是最常被忽视的功能是`hull()`。`Hull()`就像它在罐子上说的那样——在传递给它作为孩子的物体周围创建一个凸包——但这被证明是无价的。

`Hull()`解决了一批新手问题:把东西弄圆，把东西连在一起。再加上一点小聪明，`hull()`可以独自提供一个近乎完整的建模策略。如果你使用 OpenSCAD，你的作品最终会有硬边，或者你花了太多时间来计算角度，或者如果你只是想体验另一种方式来完成工作，请继续阅读！

## 圆形盒子

[![](img/355257f1bbcb3b8ac20a8c72190b995a.png)](https://hackaday.com/wp-content/uploads/2018/02/round_box_comparo.png) 有多种方法可以制作一个圆形的盒子。一种是用合适的圆柱体在周围画一个 3D 方框和 [`minkowski()`](https://en.wikibooks.org/wiki/OpenSCAD_User_Manual/Transformations#minkowski) 。另一种渲染速度更快的方法是画一个 2D 正方形， [`offset()`加上圆角边缘](https://en.wikibooks.org/wiki/OpenSCAD_User_Manual/Transformations#offset)，然后向上挤压。我甚至见过有人制作舍入工具，并将其与模型区分开来。

对我来说，最直观的方法是放置四个圆柱体作为盒子的圆边，并用`hull()`将它们连接在一起。如果你以前从未真正了解过`hull()`，这是一个很好的起点。

`Hull()`获取任意数量的对象并构建它们的凸包；这个动作就像用保鲜膜紧紧地包裹住形状，然后固化结果。为了制作承诺的圆形盒子，将`hull()`放在四个圆柱体上，四个边缘各一个。没什么好说的了，对吧？

```
points = [ [0,0,0], [10,0,0], [0,10,0], [10,10,0] ];

module rounded_box(points, radius, height){
    hull(){
        for (p = points){
            translate(p) cylinder(r=radius, h=height);
        }
    }
}
```

当然，还有更多！圆形三角形、六边形、七边形、八边形和其他边形。而且也没理由保持规律，换个角点就行了。但是对我来说，`hull()`最有用的简单应用可能是在盘子、酒吧或连杆上制作圆端。

```
module cylinders(points, diameter, thickness){
    for (p=points){
        translate(p) cylinder(d=diameter, h=thickness, center=true);
    }
}

module plate(points, diameter, thickness, hole_diameter){
    difference(){
        hull() cylinders(points, diameter, thickness);
        cylinders(points, hole_diameter, thickness+1);
    }
}

module bar(length, width, thickness, hole_diameter){
    plate([[0,0,0], [length,0,0]], width, thickness, hole_diameter);
}

```

例如，有了`bar()`和`plate()`以及詹森联动装置中所有部件的[尺寸，你就离可打印的 Strandbeest 不远了。注意这个工作流程是多么令人愉快:找出你需要你的洞的地方，把它们输入到一个点的向量中，OpenSCAD 会处理剩下的事情。谢谢，`hull()`！](https://en.wikipedia.org/wiki/Jansen%27s_linkage)

[![](img/25e91fd6ab19b942e7029e528d8781d6.png)](https://hackaday.com/linkage/)[![](img/6bfd08125cda4ecff2028e0cb0e2ec7e.png)](https://hackaday.com/mounting_plate0/)[![](img/05cefd144b8570f11356a1e8d8abd303.png)](https://hackaday.com/arbitrary_plate/)

## 将对象连接在一起

但是等等，还有呢！在上面的条板例子中，所有的点都被限制在一个平面上。如果你需要一个复杂的三维安装板，你只需将这些点推入三维空间，并在你刚刚制造的混乱之后进行清理。

```
points = [ [0,0,0], [40,0,0], [23,-10,0], [60,19,10] ];
difference(){
    plate(points, 10, 1, 5.5);
    for (p=points){
        translate(p + [0,0,1])
            cylinder(d1=10, d2=15, h=7);
        translate(p + [0,0,-1])
            mirror([0,0,1])
            cylinder(d1=10, d2=15, h=7);
    }
}

```

[![](img/0dc142a9a8b35d884869100fe72ec46d.png)](https://hackaday.com/3d_plate1/)

Move a point out of plane

[![](img/dae43ce270b843d4da4255ca297ecf99.png)](https://hackaday.com/3d_plate2/)

Clear out the holes

[![](img/8008365508563dbe2da92d1d2065d278.png)](https://hackaday.com/3d_plate3/)

Mirror for the underside

一旦你开始考虑使用`hull()`连接任意位于 3D 空间的物体，你就掌握了，我们可以留下简单的安装板。例如，我用 20/20 的铝型材做了一个植物灯架，只有一些简单的形状和一些`hull()`。

灯的腿需要连接到挤压的某个地方，所以我从一个 25 毫米的立方体开始，用轮廓打孔。接下来，脚需要着地，所以我又放置了两个足够远的立方体，这样它们就可以容纳植物的花盆。每只脚都单独固定在中心块上，模型旋转，然后送到打印机。因为我已经设计好了挤压型材，所以整个设计只花了不到 15 分钟。打印花了大约五个小时。

[![](img/d6e46e294e63719ae853c711fd06dd13.png)](https://hackaday.com/wp-content/uploads/2018/02/lamp_composite.png)

再次拯救了一个非常相似的设计问题，表面上看起来可能完全不同。我自行车灯架的一个零件坏了。对于适合灯的标签，一个简单的立方体就可以了，将支架拧到座管夹上只需要一个孔。但是如何把洞和立方体连接起来，又不用太担心形状呢？

这里的一个改进是`hull()`不能包围整个安装标签，因为它不适合灯的插槽，所以我用另一个简单的立方体为船体做了一个着陆垫，这里用红色显示。

[![](img/f49a299ca31647e20e6fae4c3ad301f3.png)](https://hackaday.com/wp-content/uploads/2018/02/bike_light1.png)

这是一个通用策略:在 3D 空间中定位你想要连接在一起的对象，在每个对象中嵌入一个着陆垫，然后根据需要将它们成对或成组地连接在一起。着陆垫的形状决定了连接器的形状，3D 对象和空间上的`hull()`的结果往往会令人惊讶，而且往往令人惊讶地优雅，因此您会想要进行实验。但是一旦你习惯于把`hull()`看作一个通用的连接器，你会发现这种技术无处不在。

## 延伸，变得有创造力

通过几个辅助函数，您可以使使用`hull()`建模变得更容易一些。例如，在上面的灯的例子中，我们需要`hull()`一只脚和中心块在一起，然后对另一只脚重复这个动作:

```
hull(){
    mount_block();
    foot_block(1);
}
hull(){
    mount_block();
    foot_block(-1);
}

```

这么多重复！那不行。同样，如果你想做出有创意的有机形状，你会发现将物体按顺序连成一条链会更方便，而不是全部放在一起。

```
module multiHull(){
    for (i = [1 : $children-1])
        hull(){
            children(0);
            children(i);
        }
}

module sequentialHull(){
    for (i = [0: $children-2])
        hull(){
            children(i);
            children(i+1);
        }
}

```

[![](img/ffa379fd87dd0c61073cc967f5e55737.png)](https://hackaday.com/wp-content/uploads/2018/02/question1.png) 这两个函数都利用了`children()`机制，可以让你将子对象嵌入到自己的模块中。`multiHull()`负责灯的情况；这是与其他每一个对象成对出现的第一个子对象`hull()`。`sequentialHull()`将第一个对象连接到第二个对象，第二个对象连接到第三个对象，依此类推。

这些函数的一个限制是，它们不能接受循环中的对象*作为子对象，因为 OpenSCAD 中的`for()`循环以一个隐式的`union()`命令结束，将循环的所有元素连接在一起。这意味着，在某些情况下，您最终将自己显式地编写出`for()`和`hull()`循环。我仍然觉得这些功能很有用。例如，灯脚代码如下:*

```
multiHull(){
    mount_block();
    foot_block(1);
    foot_block(-1);
}
```

为了展示这些功能，让我们制作一个通用的 PCB 支架——例如，如果你的桌子上有小的金属部件，你可以在任何裸板设备下放置这种东西。从安装孔的位置开始(go，go，[卡钳](https://hackaday.com/2016/04/15/measuring-parts-badly-for-accurate-reverse-engineering/)！)，`multiHull()`一些圆柱体用一个中心点连在一起做成一个十字，把它们都连在一起。如果你想要一些更实际的东西，你可以用一个`sequentialHull()`绕过一个环中的这些点，形成一个正方形的边界。最后，如果你也想保险杠墙完全摇篮的 PCB，创建两个圆边盒通过`hull()`缸，并采取他们的差异。检查[代码](https://gist.github.com/hexagon5un/0b119627e736658db186de3212fdad5f):用`hull()`、`cylinder()`、`difference()`一切搞定。

[![](img/dc55bbb34b400aaabf977bddced10ca6.png)](https://hackaday.com/wp-content/uploads/2018/02/pcb_case.jpg)

这里所有的`hull()`函数，以及其他一些函数，都在一个 [`hull.scad`文件](https://gist.github.com/hexagon5un/73e187dfa0404c69177795424f397ce6)中，这样你就可以在你的项目中包含它们，只需在你的代码顶部添加一个简单的`use <hull.scad>`。如果您使用 OpenSCAD，但是还没有完全接受`hull()`作为一个有用的建模策略，我希望这篇文章能够通过一些有用的设计模式为您指明正确的方向。尽情享受吧！