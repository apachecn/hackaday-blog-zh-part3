# 用于 3D 打印机的可变厚度切片

> 原文：<https://hackaday.com/2016/11/03/variable-thickness-slicing-for-3d-printers/>

通过适当的调整，任何 3D 打印机都可以创建非常详细的数字文件的物理副本。打印机以非常高的细节打印一个物体所需的时间完全是另一回事。层高度越低，必须打印的层数就越多，打印时间就越长。

感谢 Autodesk 集成增材制造团队的[Steve Kranz],现在有了一个解决超长、高质量打印问题的方案。它被称为 [VariSlice](https://www.youtube.com/watch?v=HAmneiL5-jQ) ，它只在需要的地方以高质量的方式分割 3D。

VariSlice 背后的基本思想是在最大层高度打印垂直墙壁，而非常浅的角度(例如球体的顶部)则在非常低的层高度打印。这是简单而明显的；你永远不需要以 10 微米的分辨率打印一面垂直的墙，精细的细节在高图层高度下看起来总是很糟糕。

就像所有 3D 打印技术一样，诀窍在于实现。在 VariSlice 的[指令中，该算法似乎一次考虑一个对象的整个层，取整个周长上的最大斜率，并在必要时调整层的高度。这里没有奇怪的楼梯踏步、不同厚度的重叠层或交错层。它会自动做你通常不得不手动](http://www.instructables.com/id/Variable-Slicing-for-3D-Printing-on-Autodesk-Ember/)[做的事情](http://manual.slic3r.org/expert-mode/variable-layer-height)。

然而，VariSlice 算法现在是 Autodesk 的开源成果之一，就像下面例子中使用的 Ember resin 打印机一样。不过，这种算法在基于细丝的打印机中的应用是显而易见的。相同质量水平的速度增加是可变的，但打印一些非常具体的对象所需的时间可以快十倍。这种算法能否集成到 Cura 或 Slic3r 中完全是另一回事，但我们只能希望如此。

 [https://www.youtube.com/embed/HAmneiL5-jQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HAmneiL5-jQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

