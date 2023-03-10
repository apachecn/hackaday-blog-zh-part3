# 黑客日奖参赛作品:改装诺基亚

> 原文：<https://hackaday.com/2017/09/12/hackaday-prize-entry-retrofit-a-nokia/>

诺基亚 3210 是有史以来最伟大的手机。电池持续了*天*，定制的彩色外壳在每个购物中心的售货亭都可以买到，它有贪吃蛇游戏，这款手机的底盘是用中子星的外壳精心制作的。它坚不可摧；这就是为什么我们现在更喜欢科技，而不是更短暂的概念，比如关系和爱情。

作为 Hackaday 奖的参赛作品，[Bastian] [将诺基亚 3210 带入了本世纪](https://hackaday.io/project/21263-nokia-3210-retro-fit-board)。他正在设计一个电路板，具有相同的占地面积、相同的按钮布局和更好的屏幕，可以直接放入 3210 可爱的塑料外壳中。

[![](img/a4642c75699f9d5932fb26d460805eef.png)](https://hackaday.com/wp-content/uploads/2017/09/routing.png)

Also known as, ‘a fun time’

升级后的 3210 目前的 BOM 包括一个 STM32 F7 微控制器，这或多或少是目前你能得到的顶级 ARM 微控制器。在无线方面，[Bastian]使用 A7 GSM/GPRS 模块和 ESP8266 来实现一点点 WiFi。对于一个哑巴来说，这是可笑的压制。如果[Bastian]能制造出一个原型并运行起来，那么这种功能如此强大、包装如此坚固的设备将会有一些有趣的应用。

Bastian 在这个项目中遇到的一个问题是 KiCad。微过孔在 KiCad 中没有正常工作，它们只限于外层。对于像这样复杂的电路板布线来说，这是一个问题，所以[Bastian] [写了一个补丁](https://hackaday.io/project/21263-nokia-3210-retro-fit-board/log/66112-small-changes-big-issue)，为 KiCad 提供了一个“我知道我在做什么”的模式，适用于任何地方的微孔。

这才是真正的 Hackaday 奖的精神:Bastian 不仅在创造一些荒谬的东西，他还在创造工具来实现它。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)