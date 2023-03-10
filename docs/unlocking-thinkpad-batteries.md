# 解锁 Thinkpad 电池

> 原文：<https://hackaday.com/2016/02/11/unlocking-thinkpad-batteries/>

几个月前，[Matt]意识到他的 Thinkpad X230T 需要另一块电池。原来的电池只能维持 10 分钟，他想要一个能维持整个飞机飞行的电池。当他的新电池到达时，他安装了它，却发现在启动时显示了一条令人不安的消息:“**系统不支持非联想制造或授权的电池。**“电池有缺口，现在[【马特】必须想办法绕过这个](http://www.zmatt.net/unlocking-my-lenovo-laptop-part-1/)。

大多数最新的笔记本电脑电池都有一个集成控制器，通过 SMBus 实现了[智能电池规范](http://sbs-forum.org/specs/sbdat110.pdf) (SBS)，这是一种类似 I2C 的协议，数据和时钟引脚就在电池连接器上。在将 USBee 逻辑分析仪连接到相关引脚后，[Matt]发现电池没有正确地向 Thinkpad 的电池控制器报告自己。

问题明确后，[Matt]有几个选择。第一种方法是打开两块电池，用新的(非正品)电池替换旧的(正品)电池。如果你曾经拆开过笔记本电脑的电池，你就会知道这是最糟糕的选择。有一些塑料和胶水，如果你足够幸运，以一种相当干净的方式把电池拆开，你就不会再把它组装起来了。第二个选择是修改非正品电池的固件。【查理·米勒】[已经对这个](https://media.blackhat.com/bh-us-11/Miller/BH_US_11_Miller_Battery_Firmware_Public_WP.pdf)做了一些研究，但是没有一个标准的 SBS 命令能在非正品电池上工作，这意味着【马特】需要把电池拆开来看看里面是什么。第三种选择是一个嵌入式控制器，它可以接入充电器连接器上的 SMBus，但根据[Matt]的说法，给笔记本电脑增加额外的电子设备并不理想。最后一个选择是修改 Thinkpad 的嵌入式控制器固件。[这最后一个选项是他用](http://www.zmatt.net/unlocking-my-lenovo-laptop-part-2/)选的。

有一个非常大的社区致力于 Thinkpad 固件破解、逆向工程，以及将 Thinkpad 改造成最好的机器。手里拿着笔记本电脑的原理图，[Matt]找到了负责电池充电的嵌入式控制器，经过几次有根据的猜测，他取得了一些成功。然而，当他在软件镜像中发现一些奇怪的加密代码时，他遇到了问题。一些俄罗斯开发人员遇到了同样的问题，通过将 JTAG 连接到嵌入式控制器芯片，这个开发人员拥有了这个芯片上所有内容的完全解密的闪存映像。

[Matt]的下一步是获取加密图像并为嵌入式控制器构建新的固件，这将使他能够为品牌外的电池充电，并且可能为地球上的所有其他电池充电。至于有趣的修改，这是正确的顶部，很快就被几十个抱怨电池 DRM 的评论所掩盖。