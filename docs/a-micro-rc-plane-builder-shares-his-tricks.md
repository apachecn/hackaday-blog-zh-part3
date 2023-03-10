# 一个微型遥控飞机制造商分享他的技巧

> 原文：<https://hackaday.com/2017/02/10/a-micro-rc-plane-builder-shares-his-tricks/>

在微型遥控飞机领域，有些人将工具、材料和工艺发挥到了极致，而[Martin Newell]对从头开始制作类似于 1:96 比例的 P-51 野马的工作进行了深入的探讨。这架小飞机完全可以飞行。它甚至包括工作导航灯和闪烁的大炮(都是用 0402 LEDs 完成的)和功能性的可伸缩起落架。它重 2.9 克，令人难以置信。除了电池，飞机上的一切都是从零开始建造或组装的。下面嵌入一个视频。

[Martin]分享了飞机上许多特殊部件所采用的一些技术。两份文件([第一部分关于用于小型飞机的技术](https://www.dropbox.com/s/owc2mq52z02zktn/Warbirds_at_1-100_Scale_Part_1.pdf?dl=0)和[第二部分关于 P-51 野马的图片](https://www.dropbox.com/s/s3w265wpt7mnqyh/Warbirds_at_1-100_Scale_Part_2.pdf?dl=0))值得一读。在真正的工匠时尚中，他意识到虽然他推出了自己的解决方案，但不知道之前有任何类似的工作，如果他的创新之前没有人做过，他会感到惊讶。

在如此小的规模下，许多问题需要重新解决，比如电连接器。所有常见的现成连接器都太大或太重，无法安装在如此小的设备上，因为一克的每一部分都很重要。只要有可能，就完全避免使用连接器，但有时——如连接定制绕组电机——必须这样做。在这些情况下，[马丁]做出了自己的选择。

![ultra-micro-connectors](img/d91275ee5bba962db6132b09e604280d.png)

微型插头和插座【来源:[比例为 1:100 的战鸟](https://www.dropbox.com/s/owc2mq52z02zktn/Warbirds_at_1-100_Scale_Part_1.pdf?dl=0)作者:马丁·纽维尔

上图左侧的插销是由一根 0.1 英寸长、直径为 0.010 英寸的黄铜棒焊接到一根导线上制成的，由 0.020 英寸内径的热缩管支撑。右边的插座是由 32 AWG 线制成的 0.1”长的塑料绝缘体，来自另一根线的线股穿过并环绕，并用 0.020”收缩管覆盖。通过挤压塑料绝缘管(右)内的多股铜销(左)实现接触。

另一项创新是方向舵、副翼和襟翼等操纵面的铰链。由于对塑料铰链不满意，[马丁]自己制作了几乎无摩擦、几乎无重量的铰链，并配有重新定心的弹簧。每个重 1.6 毫克。

![hinges](img/c9e60e5cebcffbe2356a6b2c1e6111db.png)

操纵面铰链设计【来源:[1:100 比例的战鸟](https://www.dropbox.com/s/owc2mq52z02zktn/Warbirds_at_1-100_Scale_Part_1.pdf?dl=0)作者马丁·纽维尔

左边的铰链由 0.008″镍丝和 1 毫米长 0.4 毫米塑料管制成。定心弹簧是来自画笔的尼龙鬃毛，据马丁观察，它的一端是尖的，看起来很有弹性。将单根刷毛的尖端插入模型中，通过调整其插入的距离，可以控制控制表面允许的最大偏转量。一旦满意，就用一个小胶水珠固定。![[Source: microflierradio.com]](img/bffbe2feb870cc526a448bece23a6b54.png)

一个样品微驱动器。它们变得更小了。【来源:[microflierradio.com](http://microflierradio.com/Actuators.html)

伺服系统是模型飞机上操纵舵和副翼等操纵面的常用手段，但像这样的飞机太小太轻，甚至无法携带最小的伺服系统。这些微型飞机使用微小的线圈和磁铁作为驱动器，而不是伺服系统。除非处于活动状态，否则它们不会施加任何力，这意味着无论它们连接到什么操纵面，都需要在怠速时提供自己的重新定心和保持稳定的方法。这种类型的致动器在微型飞机中很常见，但理解这种设计有助于理解为什么[马丁]以这种方式设计铰链和定心弹簧。在下面嵌入的视频中，可以在机翼底部看到类似的致动器。他们负责移动两个副翼和两个襟翼。更多的在飞机尾部的方向舵和升降舵上。

[马丁]说，到目前为止最困难的部分是可伸缩的起落架。该解决方案使用直径为 0.001 英寸的镍钛合金肌丝。肌肉导线可以拉伸大约 5%，然后当通过电流加热到临界温度以上时，它会施加相当大的力试图收缩回原来的长度。通过使用两段肌肉线，可以建立一种推拉机制，其中一根线的收缩具有拉伸另一根线的效果，同时升高或降低起落架。

![optimized-landing-gear](img/115ce1c77a5c77ac4db64fbcf6f0bff6.png)

A push-pull system using nitinol “muscle” wire provides the raw power behind actuating the landing gear, but required a significant custom assembly to work.

然而，说起来容易做起来难。[马丁]解释道:

> 不幸的是，当试图满足设计要求时，这种吸引人的简单机制充满了实现问题。其中之一是，在通过收缩一根导线来拉伸另一根导线之后，当电流停止时，收缩会弹回大约 30%。因此，需要一把锁来保持金属丝完全伸展。然后需要第二个锁来固定起落架向上或向下，这样急剧的侧向力就不会在肌肉线上产生任何力，这种力会使起落架塌陷。重量约 400 毫克的装置满足了这些要求。肌肉线将直径为 0.030 英寸的绞盘旋转 90 度。肌肉线的反冲由作用在连接到绞盘的臂的末端的惰轮上的偏心弹簧抵消。"

[Martin]在他的文档的第 2 部分[中详细介绍了起落架的整个收回组件。](https://www.dropbox.com/s/s3w265wpt7mnqyh/Warbirds_at_1-100_Scale_Part_2.pdf?dl=0)

一个常见的问题是这些飞机是否有售。答案大概也是做这种劳动密集型东西的人所熟悉的:[马丁]说不卖，至少不是从他那里买的。如果他真的把它们拿出来卖，由于工作量很大，没有人会出他的要价。

[马丁]花了大约一年的时间来开发和建造 1:96 的 P-51D 野马，他最近在他的 YouTube 频道上分享了一段小型飞机飞行的视频。它嵌在下面。

 [https://www.youtube.com/embed/0QwabcKUTuI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/0QwabcKUTuI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[Martin]在下面的视频中演示了所有 8 个控制通道:

 [https://www.youtube.com/embed/JSgRTPGYEQA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/JSgRTPGYEQA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



说到临时建造的遥控飞机，我们之前报道过一个项目，致力于为飞行的遥控飞机 3D 打印零件，并完成了深入的测试和分析。遥控业余爱好飞机是一个领域的例子，虽然充满了现成的系统，但仍然是个人创新和 DIY 精神的家园。