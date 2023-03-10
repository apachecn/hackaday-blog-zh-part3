# 这款 3D 打印显微镜的弯曲精度为 50 纳米

> 原文：<https://hackaday.com/2017/02/17/this-3d-printed-microscope-bends-for-50nm-precision/>

利用塑料的灵活性，一组研究人员创造了一种具有亚微米精度的 3D 打印显微镜。通过弯曲显微镜载物台的支架，他们可以以惊人的精度操纵样品。结合常见的 M3 螺栓和齿轮减速步进电机，他们报告了高达 50 纳米的平移运动精度。在之前，我们已经[看到了从灵活性衍生出的功能，但没有达到这个规模。而且虽然不是](http://hackaday.com/2016/09/14/3d-printed-door-latch-has-one-moving-part-itself/)[的扫描电子显微镜](https://hackaday.com/tag/scanning-electron-microscope/)，50nm 的大小也就是一个小病毒(不，不是[那种病毒](http://hackaday.com/2015/10/02/a-white-hat-virus-for-the-internet-of-things/))。

only flex 的可视区域为 8x8x4mm，在仅支持 flex 6 的情况下，这一点令人印象深刻。但是，如果 256 mm ³ 对你来说还不够，不要担心:这些设计都是开源的，并且是在 OpenSCAD 中建模的，只需要修改。只有一个文件用于打印，没有支持材料，一个[精彩的组装指南](http://docubricks.com/viewer.jsp?id=1044562654723960832)和对 PLA 和 ABS 的关注，open flex 显然是为了便于制造而设计的。光学同样有趣。使用 Raspberry Pi 相机模块，镜头反转，他们实现了一个像素对应 120 纳米的分辨率。

该组织希望他们的显微镜能够普及到世界上资源匮乏的地区，而且这种设计似乎已经开始普及。如果你想为自己做一个，[你可以在 GitHub 上找到所有必要的文件。](https://github.com/rwb27/openflexure_microscope)

 [https://www.youtube.com/embed/W_32Zb7K_KY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/W_32Zb7K_KY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

