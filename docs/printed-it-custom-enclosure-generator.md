# 打印出来:自定义外壳生成器

> 原文：<https://hackaday.com/2018/03/02/printed-it-custom-enclosure-generator/>

您已经编写了您的固件代码，蚀刻了您自己的 PCB，现在是时候将您那个令人敬畏的新项目放入机箱中了。不幸的是，你所拥有的只是一个普通的无线电窝棚项目箱，是你在他们清理库存时捡到的。如果你把你的项目放在里面，它会有一个孩子穿着旧衣服的所有风格和优雅。您的项目值得定制外壳，但是定制塑料外壳的价格和交付时间对于一次性项目来说是非常昂贵的。

在过去的日子里，下一步可能是开始弯曲一些金属板。但现在是 21 世纪了，我们这边有机械化。[Heartman] 的[“终极制盒器”是一款全参数 OpenSCAD 设计，您只需提供所需尺寸并从几个可选功能中进行选择，即可生成专业外观的外壳。几个小时后，你就可以为你的项目定制一个独一无二的外壳，只需要几分钱的灯丝。](https://www.thingiverse.com/thing:1264391)

至少，这是个想法。在这一期的“打印”中，我将通过生成和打印一个基本的附件来看看“终极制盒者”。当我到达那里时，他的无线电室已经没有外壳了，他也不想在折叠金属片时割破自己的手，所以我很想看看这种设计的效果如何。

## 配置

所以在*理论*中，这个设计应该与 Thingiverse 定制器一起工作，Thingiverse 定制器基本上只是 OpenSCAD 的 web 前端。你得到了漂亮的小滑块和对话框，一旦你输入了所有的信息，它就会呈现一个自定义的 STL 文件供你下载。关于 Thingiverse 如何工作，这可以说是 MakerBot 提出的最好的想法之一。不幸的是，在撰写本文时，Customizer 似乎不再工作，只是给出一个关于缺少`libCGAL.so.10`的错误。叹气。

[![](img/adb4371aaf871fece51cbb520b9dcdda.png)](https://hackaday.com/wp-content/uploads/2018/02/ubm_pi0render.png) 那样的话，我们就需要下载了。scad 文件，并在本地打开它。所有的配置值都在文件的顶部，并且有清晰的标签，这使得这相当容易。

显然，您将希望最小化地调整整体盒子尺寸变量。但是 PCB 支架也有一整套选项(位置、直径、螺钉尺寸等)，以及与内置通风口相关的选项。

利用 OpenSCAD `import();`函数，您可以引入一个现有 PCB 的 STL，并查看它在渲染情况下的确切外观。作为演示，我将为 Pi Zero 制作一个小外壳，因此我导入了它的 STL，并使用它来对齐 PCB 支架。但是，即使您不导入 STL 作为指导，当您在 OpenSCAD 中编辑文件时，还有一个有用的“幽灵 PCB”漂浮在机箱内。

## 导出 STL

一旦您根据自己的喜好编辑了变量，您将需要在代码中向下滚动一点，以找到如下所示的部分:

```

/* [STL element to export] */
//Coque haut - Top shell
TShell = 0;// [0:No, 1:Yes]
//Coque bas- Bottom shell
BShell = 1;// [0:No, 1:Yes]
//Panneau avant - Front panel
FPanL = 0;// [0:No, 1:Yes]
//Panneau arrière - Back panel
BPanL = 0;// [0:No, 1:Yes]

```

这些选项有选择地打开和关闭模型的不同部分，以便导出 STL。如果在导出之前没有关闭其他部分，那么得到的只是一个无用的“组装”STL。

[![](img/8d35673e542fb5328c55711ca7b447b0.png)](https://hackaday.com/wp-content/uploads/2018/02/ubm_export.png) 不幸的是，脚本不够智能，无法为 STL 导出重新定位对象；例如，你必须手动翻转切片机的顶部。我发现的另一个烦恼是，即使你关闭了外壳底部(BShell)，PCB 脚仍然存在。你需要回到脚本配置设置并手动关闭它们，寻找名为“PCBFeet”的选项。

使用 OpenSCAD 一段时间后，我知道为什么[Heartman]没有包括旋转导出部分:这是一大堆代码来实现最终用户只需点击一下他们的切片器就可以完成的事情。但是，当用户只是试图获得顶部或侧面板时，确保 PCB 支架不会呈现是一个相当大的遗漏，实际上只需要一个条件语句就可以解决。

最后，对生成定制的前后面板有一些早期支持，包括生成开口和标签的功能。但就个人而言，我建议只需将 OpenSCAD 脚本生成的空白面板导入到您熟悉的 3D CAD 程序中。在我看来，面板生成代码还没有准备好。

## 印刷

[Heartman]为这个箱子设计的设计非常巧妙，应该不会对印刷造成问题。没有突出物，所以不需要支撑，尽管如果打印机有穿线问题，你可能需要关闭通风口，因为细孔会被堵塞。我以 0.2 毫米的图层和 15%的填充率打印了我的案例，尽管为了速度，较大的案例可能会以 0.3 毫米的图层高度打印。

 [![ubm_printed1](img/738754a5c391fb01b285f220061bc85e.png "ubm_printed1")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/02/ubm_printed1.jpg?ssl=1)  [![ubm_printed2](img/c52451501b628a7fc3d3c70e3511adc7.png "ubm_printed2")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/02/ubm_printed2.jpg?ssl=1) 

该设计在公差方面是宽容的，并且在打印后不需要清理就可以将零件组装在一起。前后面板贴合完美；足够松以至于它们不需要用砂纸打磨就能进入通道，但又足够紧以至于盖子拧紧后它们不会发出嘎嘎声。顺便说一句，你必须拧紧盖子，因为这两个零件实际上没有任何互锁部件。对该设计的潜在改进将是使盖子卡扣配合的方法。

## 最后的想法

总的来说，我认为由“终极制盒者”OpenSCAD 脚本生成的外壳非常棒。它们看起来非常专业，非常坚固，并且易于打印。这绝对是一个设计，我将会把它加入到我的日常生活中。

我特别喜欢这是一个可打印的设计，它清楚地解决了一个有效的需求。一次性项目需要一次性的外壳，而 3D 打印非常适合这种情况。虽然[我们之前已经介绍过印刷工具](http://hackaday.com/2018/01/24/printed-it-rubber-band-pcb-vice/)，这些印刷工具[理应在你的工作台上占有一席之地](http://hackaday.com/2018/02/08/printed-lockable-ball-and-socket-helping-hands-plus/)，但总有人会说，你最好还是买“真货”。但是我相信这个项目提供了一个实际上在很多方面优于传统方法的解决方案。

Thingiverse 的定制者在这一点上的失误尤其令人恼火，因为[Heartman]经历了确保他的设计与它兼容的麻烦——Thingiverse 让你在 OpenSCAD 中添加一些特殊的语法，以使他们的前端工作。拥有一个基于 web 的工具来生成定制的附件将会非常方便，我想知道社区中是否有人可以接受恢复 MakerBot 似乎不支持的服务的挑战？