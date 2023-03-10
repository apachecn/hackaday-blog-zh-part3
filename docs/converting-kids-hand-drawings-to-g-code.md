# 将儿童手绘转换为 g 代码

> 原文：<https://hackaday.com/2016/05/11/converting-kids-hand-drawings-to-g-code/>

[Martin Raynsford]编写了一个[程序，将黑白 2D 图像转换成 g 代码](http://msraynsford.blogspot.ca/2016/05/drawing-to-engraving.html)，这样他的激光打印机就可以蚀刻图像。不仅如此，他还用他的激光打印机制作了一个扫描仪，其中包括一个摄像头支架和一个托盘，用于放置纸张。结果是，他把一些东西带到了最近的一次创客集会上，许多孩子在纸上画画，然后他的系统扫描并激光蚀刻。

![Screenshot of Martin's scanning and G-code maker program](img/662ade66ff8bcecaf4831a3940c06451.png)

Martin’s scanning and G-code maker program

用 C#编写的[Martin 的]程序使用 OpenGL 从网络摄像头获取图像，并逐行扫描，寻找超过对比度阈值的像素。对于每个合适的像素，程序会生成 g 代码，将激光移动到相应的坐标并烧出一个洞。查看源代码(可从他的网页下载)从注释掉的代码中可以清楚地看到，他做了大量的实验，包括根据像素的亮度改变激光燃烧时间。

虽然像[Martin]那样编写代码很有趣，但休息之后，我们将讨论一些现成的方法来完成同样的事情。

[一种选择是使用 MeshCAM](http://blog.cnccookbook.com/2014/11/10/secrets-going-cad-image-dxf-stl-gcode-cnc-3d-printing/) 或 VCarve 等软件，这两种软件都会拍摄图像，允许您根据工具进行一些修改，并输出 g 代码。在下面的视频中，珠宝是从图纸开始制作的。手机摄像头充当扫描仪，在 Photoshop 中进行细微的调整。从那里产生的人工智能文件被带入 MeshCAM 进行更多的准备，最后是 g 代码。在这个例子中，珠宝是在 CNC 机器上由黄铜切割而成的。

 [https://www.youtube.com/embed/8HGy2u1uURU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8HGy2u1uURU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



如果您的 CAD 程序具有描摹功能，那么另一个选项是将您的图像加载到 Adobe Illustrator 中，将其保存为 AI 文件，然后将其加载到您的 CAD 程序中。在那里你可以追踪 2D 图像，然后使用 CAD 程序将结果处理成适合你的工具的东西。

如果你想看另一个例子 DIY G 代码生成器，看看这个免费的 3D 建模软件 Blender add-on 叫做 Blender CAM 。

谢谢[马丁]的提示！