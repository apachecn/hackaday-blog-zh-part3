# 工业机器人、黑客和破坏

> 原文：<https://hackaday.com/2017/05/04/industrial-robots-hacking-and-sabotage/>

如今，一切都在网上，这为网络恶作剧制造了完美风暴。可悲的是，由于我们的世界联系日益紧密，即使是工业机器人设备也很容易受到威胁。趋势科技的一份新报告显示了对机器人手臂和其他工业自动化硬件的一系列攻击。

这可能看起来没什么大不了的，但是想象一下这样一个场景，攻击者故意在数千辆汽车中制造看不见的缺陷，而制造商甚至不知道。如今，汽车里的几乎所有东西都是用机械臂制造的。底盘可能造得太弱，引擎可能造得有缺陷，在预期寿命之前就会失效。甚至你的刹车盘也可能存在由电脑黑客引入的制造缺陷，导致它们在强力刹车下碎裂。前瞻性威胁研究(FTR)团队决定检查此类攻击的可行性，他们的发现令人震惊。测试是在实验室里用一个真实的工作机器人进行的。他们设法想出了五种不同的攻击方法。

[![](img/51433c223599fa451eb322ffbaaf3515.png)](https://hackaday.com/wp-content/uploads/2017/05/attack1.jpg)
**Attack 1: Altering the Controller’s Parameters**
The attacker alters the control system so the robot moves unexpectedly or inaccurately, at the attacker’s will.

*   具体影响:有缺陷或修改过的产品
*   违反的要求:安全性、完整性、准确性

[![](img/8a61c3c39b2d6c10d2d94b9418af5b18.png)](https://hackaday.com/wp-content/uploads/2017/05/attack2.jpg)
**Attack 2: Tampering with Calibration Parameters**
The attacker changes the calibration to make the robot move unexpectedly or inaccurately, at the attacker’s will.

*   具体效果:对机器人的损害
*   违反的要求:安全性、完整性、准确性

为什么这些机器人会连在一起？随着自动化工厂变得越来越复杂，维护所有系统成为一项更大的任务。该行业正在转向更多的连通性，以监控工厂车间所有机器的性能，跟踪它们的使用寿命，并在需要预防性维护时发出警报。对于其预期用途来说，这听起来很棒，但与所有连接设备一样，由于这种连接性，也存在漏洞。当您考虑到投入使用的设备经常因为各种原因(无知、经常使用等)而没有获得重要的安全更新这一现实时，这就变得尤其令人担忧。).

对于其余的攻击媒介和更详细的信息，你应该参考[报告](https://documents.trendmicro.com/assets/wp/wp-industrial-robot-security.pdf) (PDF)，这是一个非常有趣的阅读。下面的视频还展示了对这些类型的攻击如何影响制造过程的深入了解。

 [https://www.youtube.com/embed/BxHYtFlKruY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/BxHYtFlKruY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

