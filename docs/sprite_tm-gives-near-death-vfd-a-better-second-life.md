# [Sprite_tm]给濒死 VFD 更好的第二次生命

> 原文：<https://hackaday.com/2016/04/20/sprite_tm-gives-near-death-vfd-a-better-second-life/>

[Sprite_tm]捡了一些便宜的二手 VFD 显示器，想自己定制温度和空气质量显示器。当然，他这么做了，但是[把它变成了重新设计](http://spritesmods.com/?art=vfdrestoration&f=had)的巨大实验。随着几个小时的高能黑客魔咒的加入，一个 6 美元的二手 VFD 变得无价。

你看，荧光屏在旧显示器静止太久的地方有烧坏的地方。一个正常人要么接受它，要么购买新的显示器。[Sprite_tm]剥离了旧的显示驱动器，并使用 Raspberry Pi2 上的 DMA 模块驱动行和列移位寄存器，编写了自己的快速 PWM/BCM 混合方案，可以进行灰度转换。

他使用相机绘制出单个像素，并在 Gimp 中进行后处理，以确定老化像素的退化情况。然后，他重写了以前的自定义驱动程序项目，以补偿固件中像素的固有亮度。做完所有的工作后，他把整个东西包在一个漂亮的木框里。

有很多东西可以读，所以去他的网站看看吧。亮点包括基于移位寄存器的驱动程序移植、[位角度调制](http://www.batsocks.co.uk/readme/art_bcm_1.htm)，这是为灰度获得必要的位深度所需要的，以及基于照片进行亮度校正的 PHP 脚本。

挑选一个最喜欢的[Sprite_tm] hack 就像挑选一个最喜欢的冰淇淋口味:它们都很好。但是他对硬盘控制器芯片的调查仍然让我们有点晕头转向。如果你错过了他关于[和来自 Hackaday SuperCon 的电子鸡奇点](http://hackaday.com/2015/11/24/building-the-infinite-matrix-of-tamagotchis/)的演讲，一定要放下手头的工作，现在就看。