# Circuit-Sword 带来复古正义

> 原文：<https://hackaday.com/2018/04/06/circuit-sword-delivers-retro-justice/>

你不可能搜索“复古游戏”而不碰到过多的连接着各种控制器、电池等的单板计算机。通常这些项目强调功能高于一切，但[Kite]的[电路剑](https://github.com/kiteretro/Circuit-Sword/wiki)是不同的。Circuit-Sword 是基于 RaspberryPi 的复古游戏机*的核心，具有令人羡慕的适合度和光洁度。*

从根本上来说，Circuit-Sword 是一台围绕 Raspberry Pi [计算模块 3](https://www.raspberrypi.org/products/compute-module-3/) 构建的单板计算机。我们没有看到很多项目使用计算模块而不是完整的 Pi，但在这里它是一个完美的选择，允许[Kite]使用有用的外围设备，而不用携带那些对便携式手持设备没有意义的行李(我们正在看着你，以太网)。Circuit-Sword 增加了 USB-C 以快速为板载 LiPo 充电(可用的速率高达 1.5A)和适当的接头以连接特定的 LCD。计算模块省略了无线连接，因此[Kite]增加了一个 SDIO WiFi/蓝牙模块。如果你仔细观察，你可能会注意到一个外部 ATMega 调节着一组熟悉的按钮和开关。

![](img/0df4e2759464533ac56079365345d74c.png)

Optional Drill Holes

我们认为这些按钮和开关是这里最有趣的事情，因为整个电路板的设计适合原始的 GameBoy 外壳。事实证明，中国有各种各样的替换外壳(试着搜索“gameboy housing”)，还有各种各样的部件，便于安装不同的屏幕选项等等。在 wiki 的更深一层，有关于 case mod 的[指令，你可能想要执行这些指令以使一切工作最佳化。用户可以选择的选项很多。额外的 X/Y 按钮？背后有肩扣？Play Station 便携式滑动操纵杆？全部详细。对于*更多的*例子，尝试搜索](https://github.com/kiteretro/Circuit-Sword/wiki/GB-Original-Case-Mod-Guide) [SudoMod 论坛](https://sudomod.com/forum/)。例如，[这是用户【DarrylUK】的一个非常直观的构建日志](https://sudomod.com/forum/viewtopic.php?t=5268)。

case mod 的说明值得一看，即使你没有建造一个设备的意图。有一些巧妙的技巧可以帮助仔细对齐按钮和精确钻孔。预计他们的买家可能想要各种各样的选择，[Kite]在 PCB 上增加了参考钻孔，供制造商重新钻孔以安装按钮或操纵杆。为了方便添加外部状态 led，有一个小 PCB 夹具包括在内。甚至还有为完整外观添加人造游戏盒的说明。

如果你想买一个(我们当然想！)【风筝】定期做团购。查看 wiki 上正确兴趣表的链接。

感谢[Speednut Dave]的提示！