# 预拉伸织物印花融入三维空间

> 原文：<https://hackaday.com/2018/06/01/prestretched-fabric-prints-pop-into-the-third-dimension/>

在织物上打印可能是一个熟悉的技巧，但在等式中加入拉伸使我们的织物打印能够重新构建成 3D。这正是[加布]所完成的；他开发了一个脚本，[打开 3d 网格并将它们转换成六边形图案](https://n-e-r-v-o-u-s.com/blog/?p=8011)，当 3D 打印在拉伸的织物上时，让它们在放松织物时弹出 3D。

[Gabe 的]算法首先通过“边界优先展平算法”运行一个开放的 3D 表面，这给了[Gabe]一个三角形的 2D 网格。然后根据大小将三角形映射成六边形，这就产生了 2D 六边形的景观。简单地将这种六边形图案印刷到预拉伸的织物上，定义了当织物被允许松弛时将会出现的物体的形状。至于如何理解映射算法，正如[Gabe]解释的那样，“当织物在印刷后收缩时，在展平过程中经历最大收缩的区域应该经历最小的收缩，在展平过程中经历很小或没有收缩的区域应该在织物表示中尽可能地收缩。”

如果这看起来很难想象，想象一下拿一个便宜的万圣节面具，试着把它压扁在桌子上。为了将它完全压平，一些部分需要伸展，而另一些部分需要收缩。一旦变平，我们可以简单地继续拉伸，去掉所有需要收缩的部分。在这一点上，如果我们的材料非常有弹性，我们可以简单地放手，看着我们的橡胶面具跳回 3D。这就是[加布的]六边形图案背后的秘密。这些六边形的尺寸和间距限制了织物局部区域允许收缩的程度。在我们的橡胶面具的例子中，我们拉伸得最远的部分有最多的行程，所以它们应该尽可能地收缩，而在初始展平中收缩的部分(尽管我们一直拉伸，直到它们也需要拉伸)应该收缩得最少。

我们过去已经看到过一些经典的织物印花技巧。如果你渴望在织物上进行更多的 3D 打印，看看[大卫·肖雷的] [柔性织物设计](https://hackaday.com/2018/02/09/the-latest-3d-printed-fad-flexible-armor-and-pangolin-cosplay/)。

谢谢你的提示，[艾米]！