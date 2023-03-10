# 用乐高和数学制作螺旋图

> 原文：<https://hackaday.com/2017/06/29/making-spirographs-with-lego-and-math/>

乐高积木大师[大正天皇·伊索川]最近进展神速，制造出了许多机器人，这些机器人的绘画让人想起经典的 Spirograph 玩具。例如，他用乐高元素制作了一个[优雅的绘图机器人](https://www.youtube.com/watch?v=NCyy-i1UxLQ&)，见上图。乍一看，绰号“肺活量描记器”似乎是错误的，因为齿轮在哪里？然而，[大正天皇]把它们藏在纸下面，用磁铁控制笔。

[![](img/bd578bae36e3213f37735d295d5d6a1b.png)](https://hackaday.com/wp-content/uploads/2017/06/lego-spirograph.gif) 他的绘图机器人由一个平台(巧妙的，一个倒置的乐高板)组成，上面放着一张纸。一两个笔筒放在纸上，每个笔筒下面都有一对磁铁。在板的下方，两对旋转磁铁围绕双层 [11×11 弯曲齿条](https://www.bricklink.com/v2/catalog/catalogitem.page?P=24121)旋转，然后扮演经典肺活量描记器环的角色。一个由 EV3 控制的马达为整个装置提供动力。

他还使用了一个不起眼的零件——14 齿锥齿轮，最后一次由乐高在 2002 年制造，即使在那时，它也主要是以面向教育市场的零件分类出售。它是如此的晦涩难懂，乐高甚至没有在他们的在线建筑程序乐高数字设计师中提供设备，尽管(当然)T2 LDraw T3 的人们重新创造了它——它是图书馆中的 4143 号砖，见下图。

[![](img/7d6835bfd71851ac9bae629103a3fce0.png)](https://hackaday.com/wp-content/uploads/2017/05/14-tooth2.png)

### 肺活量仪齿轮数学

这个齿轮在 spirograph 风格的项目中变得很重要，因为齿数就是一切。真的没有那么多可以用乐高制作的肺活量计设计，因为齿轮的数量有限，而且它们大多具有相同的齿数——较小的齿轮有 8、12 或 16 个齿，中等的齿轮有 20 或 24 个齿，较大的齿轮有 36 或 40 个齿——看到模式了吗？这种可预测性对于一个建筑环境来说可能是很好的，但是它不会产生太多的肺活量图多样性。

计算螺旋图形状的顶点数时，取两个齿轮(或齿轮组)的最小公倍数，然后除以小齿轮。所以一个 60 齿转盘转动一对 14 齿齿轮的 LCM 是 420，你除以 28 得到顶点数:15。移除其中一个小齿轮，顶点会增加到 30 个。用 LEGO spirograph 创造新形状的挑战在于更换新的齿轮，就像原来的玩具一样，并且有更多的方法来获得不同寻常的齿轮比，从而产生更有趣的图形。

另一个让 14 齿齿轮如此吸引[大正天皇]的原因是，它是少数几个齿数不能被 4 整除的乐高齿轮之一。这意味着齿轮与相同的齿轮以 90 度角啮合。通常，齿轮在圆周的每一个四分之一处都有相同的数量，啮合就变成了一个齿轮一个齿轮地啮合。这可能是一个问题，因为乐高车轴有一个“加号”形状的轮廓，你可能不希望车轴上的所有东西都倾斜——有一个 90 度的解决方案非常有意义。

[![](img/66a92bb8d32d6aa2e823861e89319976.png)](https://hackaday.com/wp-content/uploads/2017/05/lego_spirograph.png) 【大正天皇】在[矶川工作室](http://www.isogawastudio.co.jp/legostudio/)设计乐高机器人，并撰写了几本关于[高级乐高技术](https://www.nostarch.com/powerfunctions1)的书，由 No Starch 出版。他专门研究小巧精致的机械装置——寻找毫不费力地协同工作的完美元素组合。你可以在右边的齿轮组件中看到一个例子——一对前述的 14 齿锥齿轮，在那个金色垫片的帮助下变成了一个普通齿轮，正是乐高*指环王*产品线中的一个环。你可以在 YouTube 上找到他的项目视频。

[大正天皇]已经发布了许多肺活量绘图机器人的变种。下一步是什么？也许是一个[和声图](http://hackaday.com/2017/02/22/harmonographs/)？

 [https://www.youtube.com/embed/NCyy-i1UxLQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/NCyy-i1UxLQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



另见他同样令人印象深刻的圆形图案图 3r:

 [https://www.youtube.com/embed/1qq9A4JEI_E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1qq9A4JEI_E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

