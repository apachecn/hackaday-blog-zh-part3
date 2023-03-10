# 本周失败:我是如何杀死 HiPot 测试者的

> 原文：<https://hackaday.com/2016/12/29/fail-of-the-week-how-i-killed-the-hipot-tester/>

您是否曾经将一台测试设备连接到电路或工作台上的一台设备上，但当您通电时，却发现可怕的魔烟冒出？对他来说不幸的是，烟雾不是来自他正在测试的电路，而是来自一台 2300 Clare H101 HiPot 测试仪。他的文章详细描述了他对罪魁祸首的搜寻，然后审视了制造商可能是如何保护该仪器的。

[Steaky]的雇主使用 HiPot 测试仪检查相邻电路是否充分隔离。在两个电路之间加一个高电压，测量两个电路之间的漏电流。在同一个设备上进行各种测试，手头的任务是生产一个新版本的开关盒，用软件控制在不同的测试之间切换。

这个特殊的仪器有一个保护电路，一对触点，在它继续工作之前必须闭合。因此，开关盒结合了一个继电器来关闭它们，电线连接到保护插座。起初，人们认为电路可以在电源电压下运行，但当发现只有 5V 时，决定在开关盒上使用 3.5mm 插孔。不经意间，它的套管接地，造成 HiPot 测试仪中的直流-DC 转换器短路，并释放烟雾。幸运的是，转换器可以被更换，机器恢复了活力，但它留下了关于内部电路设计的问题。实际上，逻辑电平读出线连接到低电流电源，即使是最基本的保护电路也能挽救局面。

我们都被警告要对这种问题保持警惕，承认这一特殊的失败并写下如此好的分析，这值得称赞。

我们的“一周失败”系列有足够的内容来娱乐那些不容易紧张的读者。这不是第一次出现连接器接线的可疑点[，而不是](http://hackaday.com/2016/03/06/fail-of-the-week-battery-pack-jack-wired-backwards/)[意外短路](http://hackaday.com/2015/10/13/fail-of-the-week-marginally-documented-pad-shorts-to-maskless-pcb/)或者甚至是一些[魔法烟雾](http://hackaday.com/2014/04/03/fail-of-the-week-cplds-that-release-blue-smoke/)的故障。

* * *

![2013-09-05-Hackaday-Fail-tips-tile](img/a4d7520e2fae140e74a0c50947218b84.png)**Fail of the Week is a Hackaday column which celebrates failure as a learning tool. Help keep the fun rolling by writing about your own failures and [sending us a link to the story](mailto:tips@hackaday.com?Subject=[Fail of the Week]) -- or sending in links to fail write ups you find in your Internet travels.**