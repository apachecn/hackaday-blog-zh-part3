# 开源手表 OSWatch

> 原文：<https://hackaday.com/2015/12/13/oswatch-an-open-source-watch/>

如果你是一个焊接忍者，擅长处理微小的部件和模块，请查看由[乔纳森·库克]打造的[开源手表 OSWatch](http://oswatch.org/) 。开始这个项目时，他的目标是让它兼容 Arduino，为未来的应用程序提供足够的内存，一次充电可以持续一整天，将 ble 用作中央或外围设备，并且体积小。凭借一些独创性、3d 打印和黑客技能，他能够完成所有这些。

OSWatch 仍然是一项正在进行中的工作，随着[详细的构建说明](http://oswatch.org/mkII_build_page_1.php)可用，它对其他人开放，可以挖掘并创建他们自己的修改版本——你只需要对构建有很大的耐心。这款手表是围绕一个 Microdunio Core+板、一个有机发光二极管屏幕、BLE112A 模块、振动电机、几个 LED 和按钮以及一系列其他部件构建的。看看这里的[示意图](http://oswatch.org/mkII_build_schematics.php)。这款手表需要 3V3，8MHz 版本的 Microdunio Core+(以确保更低的功耗)，如果这不是现成的，[乔纳森]向[展示如何修改 5V，16MHz 版本的](http://oswatch.org/8mhz_microduino.php)。

![page_1_parts](img/9a5b80c138456cef12617779f157e41d.png)

一组 [3D 打印零件](http://oswatch.org/files/parts.zip) [ZIP 文件]将所有零件打包在一起。由[Jonathan]编写的一个详细的说明子集向你展示了[如何从原始的 3D 打印零件到看起来光滑的手表外壳](http://oswatch.org/3d_printing_build.php)。本指南本身就是一个很好的资源，展示了许多关于后处理 3D 打印零件的技巧。他展示的一个技巧是如何使用烙铁加热的螺钉在 3D 打印塑料中创建一个埋头凹槽。对于显示器，他使用了单色有机发光二极管屏幕，因为它容易获得且成本低。但他在[显示选项](http://oswatch.org/details_screen.php)下列出了几个其他设备，以防你想使用清晰的记忆显示屏或彩色有机发光二极管屏幕。在他的 [Github repo](https://github.com/donothingbox) 上，你会发现 Arduino 代码以及一个基本的 iOS 应用程序。

当你完成大部分组装时，你最终会有三层——“背面”包含电池、充电端口、振动电机和几个分立零件,“中间”包含电子模块、按钮、编程端口,“正面”包含显示屏和几个 led。将所有这些放在一起，你就可以炫耀你的 OSWatch 了。我们喜欢这个项目的是由[Jonathan]提供的构建说明和细节的绝对水平，它让任何拥有合适技能的人都可以复制他的工作。如果你想看看更多的智能手表选项，这里有[开源智能手表](https://hackaday.io/project/6833-open-source-smart-watch)、 [OSHWatch](https://hackaday.io/project/2263-oshwatch) 和 [Zerowatch](https://hackaday.io/project/6855-zerowatch) 。