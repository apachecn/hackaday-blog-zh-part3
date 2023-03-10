# 将 GameCube 控制器转换为 USB

> 原文：<https://hackaday.com/2016/03/22/converting-a-gamecube-controller-to-usb/>

GameCube 控制器是新老游戏机爱好者的最爱，随着任天堂最近发布了这款控制器的 Smash Bros. edition，这是一款已经生产了非常非常长时间的控制器。[Garrett]喜欢在他的 PC 上使用 GameCube 控制器，但这需要一个笨重的 USB 适配器，或者一个品牌外的 GameCube“风格”控制器，这就需要一些东西。没有妥协，[Garrett] [将他的 GameCube 控制器变成了一个带有定制 PCB 和一点编程的原生 USB 设备](http://electricexploits.net/gamecube-controller-usb-conversion-mod/)。

第一，硬件。[加勒特]转向 ATtiny84。这个芯片是无处不在的 8 针 ATtiny85 的老大哥。电路板的设计不到一平方英寸，包括来自控制板的 USB 差分对、5V 信号和地的连接。

软件栈包括用于 USB 固件更新的[微核引导程序](https://github.com/micronucleus/micronucleus)和处理 USB 协议的 [V-USB](https://www.obdev.at/products/vusb/index.html) 。甚至还有一些受[加勒特]早期的[神威控制器模块](http://electricexploits.net/shinewave/)启发的新增功能。这种控制器模式将 GameCube 控制器变成一团炽热的乱麻，一定会在玩《超级粉碎兄弟》时分散你的竞争对手的注意力。这是一个很好的模式，因为[Garrett]保持了电路板的可焊性，所以它可以很容易地改装到任何 GameCube 控制器中。