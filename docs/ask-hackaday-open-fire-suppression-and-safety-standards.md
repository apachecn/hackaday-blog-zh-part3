# 问黑客日:开放灭火和安全标准

> 原文：<https://hackaday.com/2016/04/12/ask-hackaday-open-fire-suppression-and-safety-standards/>

我们不久前发布了一个关于 3D 打印机的帖子。一位参加中西部说唱艺术节的人把他的打印机放在一边，结果在他回来的时候发现它被烧毁了。本着开源的精神，很自然地，他和我们其他人分享了他的经验。在我看来，黑客从来都不是无能为力的，他们有积极的事情要做，也有探索的途径。

[![An animation of a commercial fires suppression system, fire trace's, operation. http://www.firetrace.com/fire-suppression-systems/direct-release-systems/](img/ccb2f5bb8af66dfe1a035e2f129a3694.png)](https://hackaday.com/wp-content/uploads/2016/03/dlp_fire.gif)

An animation of a commercial fires suppression system, fire trace’s, operation. [Firetrace](http://www.firetrace.com/fire-suppression-systems/direct-release-systems/)‘s website has more.

外面有非常棒的商用灭火系统。一种通常用于橱柜和加工中心的实施方式是通过连接的储罐用灭火剂加压的塑料管。当火灾发生时，管子在最热的地方熔化，自动向该区域喷洒灭火剂。这种方法的变体包括一个金属喷嘴，里面装满了在一定温度下熔化的蜡或塑料，就像头顶上的消防喷头一样。

该系统也成功地用于发动机舱内。例如，亚马逊上的这个[商品，只不过是一个一端有计量器的加压塑料管。由于发动机舱内部可以被视为一个封闭的空间，所以只需要很少的灭火剂就可以扑灭意外的火焰。值得注意的是，该系统在高温环境下工作，如发动机舱，这对于 3D 打印机上的封闭建筑信封来说是一个好兆头。](http://www.amazon.com/BlazeCut-Automatic-Suppression-Automotive-Extinguisher/dp/B00D7M3E7O/)

[![BlazeCut Automatic Fire Suppression System 6' TV200FA, Automotive Extinguisher](img/70f7c9bfd6c636fdc68ae09c65063c59.png)](https://hackaday.com/wp-content/uploads/2016/03/91j4osydial-_sl1500_.jpg)

BlazeCut Automatic Fire Suppression System 6′ TV200FA, Automotive Extinguisher Installed under Car Hood.

另一个选择是建造一个抑制地雷。一家日本公司和一家泰国公司都推出了可投掷灭火器。在日本的装置中，灭火器的外部是一个易碎的玻璃瓶，在受到冲击时会破碎；释放代理。泰国的装置看起来像一个排球，加热后释放药剂。这款设备似乎更适合 3D 打印或家庭项目。想象一个小的长方形包装，一面有粘合剂，放在打印机可能着火的地方，比如床下或喷嘴上方。发生火灾时，外壳会融化，系统会自动喷洒灭火剂。

这些建筑中使用的大多数化学物质都是无害的，容易获得。高压油管和蜡都可以购买，所需的熔点可以根据需要与数据表保持一致。塑料薄膜并不难获得。这些提供了一个很好的解决方案，因为它们完全是被动的。它们不需要电力就能运行，完全依赖于构成它们的材料的特性。

在主动系统中还有其他选择。Hackaday 的读者提出了一些建议，比如添加火焰传感器，以便在发生火灾时自动切断电源。在某些情况下，也可以考虑热熔断器。还有其他一些技巧，虽然不太合适，但仍然有效。例如，将关键的电线、保险丝或部件放置在可能着火的路径上，使其首先被破坏，从而快速停止设备的运行。应该探索这些途径。至少应该有一个项目使用 Raspberry Pi 和 Arduino 来发布灭火失败和房子着火的消息。

[![fire-extinguishing-balls](img/2604b7c6b5e6f968b15ff9896e4b222f.png)](https://hackaday.com/wp-content/uploads/2016/03/fire-extinguishing-balls.gif)

The [Thai invention](http://geekologie.com/2016/03/firefighting-fun-throwable-fire-extingui.php) is a volleyball that melts upon contact with flame and releases a pressurized extinguishing agent.

一些大问题是从法律和道德的角度来问的。如果有人开始销售 DIY 灭火系统的工具包，尽管有设备，但火灾最终摧毁了某人的财产，谁应该负责？张贴说明安全吗？如果一个工具箱过早地引爆并伤害了某人。我想这些专业系统的大部分成本是某种责任保险和认证。尽管如此，在一台 600 美元的打印机上安装一套 600 美元的灭火系统似乎很傻，有总比没有好。

最后，这些评论将大量的高射炮火对准了认证系统。开源项目没有理由不能产生自己的安全规范。一个没有代理的开源规范自然不能提供合法的财产损失防御，但是一个深思熟虑的测试程序可以提供一些思路。例如，在 3D 打印机的情况下，人们可以有一套基本的故障安全测试。一个例子是将打印机升温并快速断开热敏电阻，打印机会着火吗？没有吗？很好，符合规格。我不介意知道 Marlin 的最新版本是在流行的板上测试的，并且仍然符合社区的消防安全规范。

据我所知，在开源安全系统或提供测试框架以确保开放硬件满足基本安全条件方面，工作做得很少。你们中的许多人都有使用这些系统的经验。你们中的一些人经历了完全不愉快的获得 UL 认证的过程。Hackaday 是怎么想的？