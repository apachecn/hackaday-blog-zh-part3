# 打造自己的安卓智能手机

> 原文：<https://hackaday.com/2018/05/10/build-your-own-android-smartphone/>

让我们先弄清楚这个问题——这个项目并不是要取代你的普通智能手机。虽然，至少，如果你愿意，你可以把它当作一个。但是[Shree Kumar]的 2018 年 Hackaday Prize 参赛作品,[Kite:Open Hardware Android smart phone](https://hackaday.io/project/42944-kite-open-hardware-android-smartphone)旨在成为黑客和其他所有人的开放平台，使他们能够挖掘智能手机的内部结构，并将其作为基础平台来构建各种硬件。

当谈到模块化智能手机时，谷歌的 Project Ara 和 Phonebloks 项目立即跃入脑海。风筝在概念上是类似的。它允许您连接黑客友好的模块和分解电路板，例如传感器或显示器，以创建您自己的定制解决方案。由于操作系统不依赖于任何特定的品牌风格，你也可以定制和调整 Android 以适应特定的需求。没有运营商锁或服务要担心，引导加载程序解锁。

![](img/2fab76852aca3689864d95b1a3e8009b.png)

Hackaday Show-n-Tell in Bangalore

该项目的核心是 kite board——填充了通常塞在智能手机包装中的所有元素——内存、LTE/3G/2G 无线电、micro SIM 插槽、GPS、WiFi、BT、FM、电池充电、加速度计、指南针、陀螺仪和 micro SD 插槽。KiteBoard 的第一个版本是基于 Snapdragon 410 的。在班加罗尔的一次黑客聚会上受到一些微妙的刺激后，[Shree]转向了光明的一面，并决定将 [KiteBoard V2](https://hackaday.io/project/42944/log/145975-a-sneak-peek-into-kite-v2) 开源。新主板将采用骁龙 450 处理器和许多其他升级产品。Kite 项目中的第二个 PCB 是一个显示板，它将 5”触摸屏 LCD 连接到主 KiteBoard。黑客感兴趣的是在这块板上增加了一个 1080p HDMI 输出，让你[轻松地将其连接到外部显示器](https://hackaday.io/project/42944/log/137235-kite-has-hdmi-convergence-ahoy)，还允许访问 MIPI DSI 显示接口。

最后，还有扩展板，它提供了所有令人兴奋的黑客攻击的可能性。它有一个兼容 Raspberry Pi 的 HAT 连接器，GPIO 参考电压为 3.3V(kite board 工作电压为 1.8 V)。例如，如果需要连接 Arduino，GPIO 也可以参考 5 V 而不是 3.3 V。所有其他电话接口都可以通过扩展板访问，如扬声器、麦克风、耳机、电源、音量调高/调低，以方便黑客攻击。扩展板还提供对所有常用总线接口的访问，如 SPI、UART、I C 和 I S。

为了展示风筝项目的能力，[Shree]和他的团队已经制作了几个[手机](https://hackaday.io/project/42944/log/88691-building-poorna-your-first-kitephone)和[小工具](https://hackaday.io/project/42944/log/138229-pianophone-with-loud-music)变种。他的几个项目日志中记录了 3D 打印外壳和其他部件的构建说明和设计文件。BoM 的很大一部分由现成的组件组成，而不是三个风筝板模块。如果你有[功能要求](https://hackaday.io/project/42944-kite-open-hardware-android-smartphone/log/144379-feature-requests-in-the-democracy-of-kite)，风筝团队期待听到你的声音。

谈到智能手机设计，数量是游戏的名字。无论你是在和高通谈骁龙，还是和其他供应商谈内存、收音机、显示器和其他关键产品，你都需要在最小起订量上遵循他们的路线。除此之外，还需要认证世界各地各种标准的风筝板，人们意识到制造这样一款手机与其说是技术挑战，不如说是财务挑战。风筝团队实现目标的唯一方法是通过 Kickstarter 活动来获得支持和承诺，以确保他们有足够的人数来实现这个项目。看看他们，给他们一些爱。Hackaday 奖的评委们已经展示了他们的才华，从第一轮进入决赛的 20 个项目中选出了这个项目。

 [https://www.youtube.com/embed/hanbZVkot7k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hanbZVkot7k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)