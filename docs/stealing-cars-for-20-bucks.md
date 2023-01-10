# 为了 20 块钱偷车

> 原文：<https://hackaday.com/2017/04/27/stealing-cars-for-20-bucks/>

[曾英涛]、[杨庆]和[李峻]，又名[独角兽团队]，开发出了迄今为止最便宜的破解被动无钥匙进入系统的方法，这种方法在一些汽车上可以找到:大约 22 美元的零件，上下浮动 1 美元。但这还不是全部，他们设法将此前已知的这种攻击的有效范围从 100 米增加到 320 米左右。几周前，他们在 HITB 阿姆斯特丹做了一次演讲，并展示了他们的成果。

这种攻击本质上并不新鲜，它基本上只是为密钥卡创建了一个范围扩展器。一个无线电放在汽车附近，另一个放在汽车钥匙附近，这两个无线电将来自汽车的信号传递给遥控钥匙，反之亦然。这个版本的黑客脱颖而出，因为[UnicornTeam]对恩智浦生产的无钥匙进入系统信号进行了逆向工程和解码，因此他们可以通过他们选择的任何通道发送解码信号。据我们所知，唯一的限制是传输超时。这一切必须在 27 毫秒内发生。你几乎可以通过互联网而不是无线电来完成。

实际的键码没有被破解，就像在 HiTag2 攻击中一样。这也不像[黑掉一个滚动密钥卡](http://hackaday.com/2014/03/17/hacking-rolling-code-keyfobs/)。信号只是在两个设备之间被嗅探、解码和中继。

研究人员建议的解决方法是减少 27 毫秒的超时时间。如果它足够短，至少这些类型的攻击的距离会减少。即使这最终可以减轻或减少攻击对新车的影响，旧车仍然存在风险。我们建议从一开始就打破被动无钥匙系统:允许智能钥匙在没有任何用户交互的情况下打开和启动您的汽车是自找的。汽车司机真的懒到不能按一个按钮解锁汽车吗？无论如何，如果你被困在这些系统中的一个，看起来唯一可靠的退路是锡纸帽。当然是为了钥匙链。

[通过[连线](https://www.wired.com/2017/04/just-pair-11-radio-gadgets-can-steal-car/)