# 用编码器增加 OpenSCAD 的直观性

> 原文：<https://hackaday.com/2017/11/01/add-intuitiveness-to-openscad-with-encoders/>

我第一次看到 3D 建模和 3D 打印实际应用是在一次黑客日活动上。我们打印了简单的塑料支柱来分开几根装有弹簧的电线。就零件而言，没有什么革命性的，但那一刻我意识到了打印机的价值。

从那以后，我一直使用 OpenSCAD，因为这是我第一次看到的，但其他程序的直观性让我开发了 [OpenVectorKB](http://24hourengineer.com/2017/10/2017-10-29-su-vector-editing-keyboard.html) ，它允许 OpenSCAD 中无处不在的向量被随意更改，同时保持程序的参数化质量，甚至利用它们。

矢量中的所有三个值 X、Y 和 Z 都可以通过旋转编码器旋钮来修改。该设备充当键盘，用于

1.  选择相关的值
2.  用更新的值替换它
3.  刷新显示
4.  将光标移回起点

不需要安装软件，它运行在一个 Teensy-LC 上，因此在旋转编码器可能有用的任何程序中，为其他程序重新编程是可能的。其他模式包括鼠标、箭头键、Audacity 编辑控件和 VLC 时间搜索。

这里有[一篇支持 OpenSCAD](http://hackaday.com/2013/12/11/3d-printering-making-a-thing-with-openscad/) 的文章，这里有[一篇反对](http://hackaday.com/2017/01/03/ditch-openscad-for-c/)。这篇文章很好地解释了[OpenSCAD](https://hackaday.com/2012/08/20/rendering-openscad-in-the-browser/)。

 [https://www.youtube.com/embed/yZbAFO5v-is?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/yZbAFO5v-is?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[编者按:这是 Hackaday 作家的 hack，因此用“我”代替通常的“我们”。虽然我们都喜欢定制外设，我们中的许多人也喜欢 OpenSCAD，所以你可能会以任何方式阅读它，但我们不想为[Brian]的工作邀功。]