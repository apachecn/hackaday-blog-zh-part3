# 超级徽章黑客快速入门

> 原文：<https://hackaday.com/2017/10/20/supercon-badge-hacking-quick-start/>

迈克·哈里森(Mike Harrison)为今年的黑客日超级大会(Hackaday Superconference)设计的硬件徽章正乞求被黑客攻击。今天，我想帮助你尽快恢复健康。

Supercon 的黑客村氛围今年提前一天开始。11 月 10 日星期五，中午开始领取徽章，整个下午都在继续徽章黑客活动，然后当晚在 Supplyframe 总部举行派对。计划星期五去镇上，一起去玩。当然，如果你还没有，你需要[买一张超级机票](https://supercon2017.eventbrite.com/?aff=hadcom1020)。

查看[2017 超级大会徽章项目页面](https://hackaday.io/project/27427-camera-badge-for-supercon-2017)，获取 Mike 在开发过程中整理的完整文档。

### 硬件黑客

[![](img/62501697c7666f1bbcfad3584ed95c90.png)](https://hackaday.com/wp-content/uploads/2017/10/supercon-badge-hardware-hacking.jpg)

This is the first prototype, the finished badge will have solder mask

**注意事项:**原型区域，2×6 扩展头，ISP 头，TTL232 头

**详细硬件黑客细节:** [项目日志](https://hackaday.io/project/27427-camera-badge-for-supercon-2017/log/68570-hardware-hacking)

想转板的，看扩展头。它将 I2C 线、RX1/TX1 的串行线和四条额外的 GPIO 线分开。该集管为 2×6 通孔，间距为 0.1 英寸。这些徽章头是空的，但可以焊接在超级会议的徽章黑客区。

如果你是硬核，你可以使用电路板上的原型区域来焊接你的元件。就在这个标题上方，你会发现一排垫提供 I2C 和电力。

该徽章将有两个填充的标题，无论您是攻击硬件还是软件，都可能会感兴趣。在电池座旁边，您可以看到 0.1 英寸的 SIL 引脚，顶部有 ISP 头(使用 PICkit 而不是复制到 SD 卡和使用引导加载程序的程序)，下面有 TTL232 头，这有助于监控调试信息。

Mike 在固件中包含了一些帮助函数，用于控制转接接头上的引脚。查看以上链接的硬件黑客部分，了解更多相关信息。

### 软件黑客

![](img/61cbb06186cdd184706a89fcb2a0ebb6.png)

Screenshot of apptemplate.c

**注意事项:**你需要在电脑上安装免费的 [MPLAB-X IDE](http://www.microchip.com/mplab/mplab-x-ide) 和 [XC32 编译器](http://www.microchip.com/mplab/compilers)。编译好的十六进制代码可以复制到 badge micro SD 卡上，用 bootloader 刷新，或者使用编程器(即:PICkit3)。

**详细的软件黑客细节:** [项目日志](https://hackaday.io/project/27427-camera-badge-for-supercon-2017/log/68569-firmware-hacking-and-adding-new-applications)

Mike 已经编写了一个非常棒的软件框架，使得开始使用徽章变得非常容易。他的代码负责管理所有的硬件，并提供了一个 apptemplate.c 文件，可以作为你每次攻击的开始。他甚至有一个简单的方法让你将你的每一个黑客添加到徽章菜单中，以便于显示。

app 模板包括一个状态机，当程序启动时，它将运行一些设置代码(s_ start)，然后一个不同的代码块在一个循环中运行(s_run)。每隔 20 毫秒设置一个滴答标志，以便于计时。

用户输入包括 6 个按钮、一个加速度计和摄像头，输出包括一个 128×128 彩色有机发光二极管屏幕和一个白色 LED(摄像头“闪光灯”)以及上面硬件部分描述的数据总线。处理器非常快，并且有大量的闪存和 RAM 可用。

### 开始考虑组队吧！

一个伟大的想法总是任何黑客攻击中最难的部分。开始在超级会议聊天上抛出一些想法。