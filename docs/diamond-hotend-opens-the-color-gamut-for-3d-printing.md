# Diamond Hotend 开启 3D 打印色域

> 原文：<https://hackaday.com/2015/11/18/diamond-hotend-opens-the-color-gamut-for-3d-printing/>

可以肯定地说，我们在使用 FDM 技术的基于爱好的 3D 打印机方面已经到达了一个高原。打印质量相当高，速度也快得差不多了，而且与商用机器相比，它们非常物有所值。那么下一步是什么？[彩色打印怎么样？](http://reprap.org/wiki/Diamond_Hotend)

使用普通的 3D 打印机和一点耐心可以打印出彩色图像[，但这真的不经济也不高效。我们也看到了用于 3D 打印的多个挤出机头，但由于校准和塑料从一个机头到另一个机头的拖尾，这存在许多问题。那么，如果你可以将多种颜色的细丝放入一个混合头中会怎么样呢？](http://hackaday.com/2015/04/06/3d-printing-different-colors-with-a-single-extruder/)

事实证明你可以。今年早些时候，RepRap 为钻石酒店的开发运行了一个 Kickstarter。它现在已经投入生产，看起来运行得很好。它还与许多 3D 打印机兼容，只要主板支持三重挤压。

然而，一个大问题仍然存在——你如何规划一个彩色打印？实际上使用重复的主机。您需要在[中导出您的 3D 模型。AMF 文件格式](http://reprap.org/wiki/Amf_file#AMF)，但一旦你这样做，你将能够[配置它在 Repetier 主机内的彩色打印工作。](http://reprap.org/wiki/Diamond_Hotend#Multi-material_printing_with_Repetier_Host)

 [https://www.youtube.com/embed/sCkK9oUHncQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/sCkK9oUHncQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



或者，您可以用单色打印所有内容，然后使用[水文印刷技术在您的印刷品上印上全色图像……](http://hackaday.com/2015/05/13/printing-photorealistic-images-on-3d-objects/)

[通过[t0 运动]