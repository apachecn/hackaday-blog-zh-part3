# 开源 SNES 到 USB 转换器让你合法地模仿

> 原文：<https://hackaday.com/2016/08/28/open-source-snes-to-usb-converter-lets-you-emulate-legally/>

[ Andrew Milkovich]受到启发，基于我们在 【互联网时代】[前](http://hackaday.com/2009/06/19/usb-reader-for-snes-game-carts/)报道过的一款设备，打造了自己的[超级任天堂读卡器](https://github.com/amilkovich/snes-rd)。该设备安装了一个真正的卡带作为 USB 大容量存储设备，允许您直接从推车上使用模拟器玩游戏。

它的核心使用了 Teensy++ 2.0。[Andrew]不得不将 EEPROM 引脚从 SNES 盒式磁带上拆下来，并自己对引脚进行逆向工程，但最终结果是一个可以成功读取盒式磁带而不擦除它的设备，这是一个不小的成就。完成的盒式磁带阅读器是建立在一些原板上的，我们想补充[Andrew]在那块板下面的跳线路由。

当然，没有[原控制器](https://github.com/amilkovich/snes-pad)，任何主机的体验都是不一样的。所以[Andrew]更进一步，制作了他自己的 SNES 控制器到 USB 转换器。它的核心是古老的 Atmel ATmega328，如果需要的话，可以与盒式读卡器分开使用。