# 在鹰板上安装 3D 打印

> 原文：<https://hackaday.com/2015/10/25/fitting-3d-prints-on-eagle-boards/>

你要做的最困难的事情之一就是将你的电子设计和机械设计结合起来。在正确的位置为开关打孔是一件痛苦的事情，如果你做得足够多，你会发现面板安装插孔的美丽。当使用 Eagle 设计 PCB 时尤其如此，但通过一些技巧，[可以直接从 Eagle designs](http://discspace.org/generating-3d-printable-pieces-directly-from-eagle-pcb-designs/) 构建 3D 可打印件。

[泰勒]用一束发光二极管做了一个时钟。虽然时钟工作得很好，但在他定制的七段数字段周围有很多漏光。解决方案是一个光罩，泰勒在鹰中找到了如何制作光罩的方法。

第一步是在鹰板上画一个新层，定义光掩膜。这在 CAM 处理器中导出为 EPS 文件，为他提供了 2D 绘图。至少是按比例的。

下一步是安装 Inkscape，安装[paths 2 penscad](https://github.com/l0b0/paths2openscad)。这将二维绘图转换为 2D 对象，可以在 OpenSCAD 中渲染并导出为 3D 可打印 STL 文件。

这个项目有效吗？结果很棒——整个光罩是一个单壁印刷，由于这种光罩不需要任何机械强度，它应该保持得很好。时钟看起来比以前好多了，而且[泰勒]有了一种为他的 2D 印刷电路板制作 3D 物体的新技术。