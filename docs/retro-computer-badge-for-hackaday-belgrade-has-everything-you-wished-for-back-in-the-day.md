# 贝尔格莱德 Hackaday 的复古计算机徽章拥有您过去想要的一切

> 原文：<https://hackaday.com/2018/05/15/retro-computer-badge-for-hackaday-belgrade-has-everything-you-wished-for-back-in-the-day/>

Hackaday 贝尔格莱德会议的硬件徽章是一台复古电脑，你可以戴在脖子上。我手里就有一个，它真的是一件艺术品。它很漂亮，玩起来很有趣，它将成为一个辉煌的徽章黑客周末的史诗平台！看看第一个视频，然后和我一起深入了解细节。

[立即购买我们在本月底举办的顶级欧洲硬件会议——贝尔格莱德 hack aday](https://www.eventbrite.com/e/hackaday-belgrade-2018-tickets-42286732756?aff=hadcom0515)的门票。这是一个充满了谈话、工作、食物和娱乐的日子，当然，每个进门的人都会得到一枚这样的徽章。最精彩的部分是这个社区，包括晚上举行的黑客村。我们将在硬件演示、演示、闪电对话以及现场 IDM 和 DJ 节目中破解徽章，直到凌晨。

 [https://www.youtube.com/embed/4ZOwflpJq4U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/4ZOwflpJq4U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



## 可爱的硬件

这个徽章感觉不可思议。概念和硬件设计是 Voja Antonic 的工作，他已经在贝尔格莱德确保制造过程顺利进行。因为每个参加会议的人都会得到一个徽章，所以有很多硬件要生产！

 [![hackaday-belgrade-badge-prototype-front](img/c9f2b303e30b719245da98a497f65913.png "hackaday-belgrade-badge-prototype-front")](https://hackaday.com/2018/05/15/retro-computer-badge-for-hackaday-belgrade-has-everything-you-wished-for-back-in-the-day/hackaday-belgrade-badge-prototype-front/)  [![hackaday-belgrade-badge-prototype-rear](img/8ca99e4ff03397a4030ddc9a6391abf3.png "hackaday-belgrade-badge-prototype-rear")](https://hackaday.com/2018/05/15/retro-computer-badge-for-hackaday-belgrade-has-everything-you-wished-for-back-in-the-day/hackaday-belgrade-badge-prototype-rear/) 

Voja 是在他的设计中包含巧妙选择的大师。我喜欢这个徽章的形状，挂绳孔在一边。但是相对的角有一个轻微的斜面，把形状拉向一个非常有趣的方向，还有柔和的圆角。有角度的开关以一种直网格不会有的方式引人入胜，Voja 选择在顶部铜中添加交叉阴影线的地面浇注给人一种令人愉快的纹理，你可能没有注意到，但如果把它拿走就会错过。这个徽章是华丽的。

当我想到复古电脑时，脑海中浮现的是一个点击键盘和一个绿色(或琥珀色)单色显示器。这个徽章轻松满足键盘爱好者的 55 个瞬间按钮。屏幕本身是全彩色的，所以*可以*做单色，在 320×240 时，它有一种低分辨率 CRT 的感觉，默认情况下以 40×20 字符 VT100 模式运行(在软件部分有更多信息)。

让你会心一笑的惊喜是背面的 PCB 安装扬声器。它可以用三种声音驾驶，听起来棒极了！你会发现前面有一个 RGB LED 模块，以及一个用于编程、串行、I2C 和一些 GPIO 的扩展接头。所有这些都是由 PIC32MX370F512H 以及一个用于存储程序的 2mb 闪存芯片驱动的。如果这一切在过去都可以作为一台计算机使用，它将统治整个行业:48 MHz，512 kB 闪存和 128 kB RAM。

我拥有的徽章是 5 个“mark 2”原型之一——原始版本没有扬声器，基于 PIC24 芯片，这个版本从 AAA 升级到 AA。生产徽章有黑色阻焊膜和背面的丙烯酸挡板，但其他一切都保持不变。在[页面项目页面](https://hackaday.io/project/80627-badge-for-hackaday-conference-2018-in-belgrade)了解更多信息。

## 令人愉快的软件

[![](img/4ab765c947329cb2331a6965b8022604.png)](https://hackaday.com/wp-content/uploads/2018/05/dsc_0866.jpg)

Music scripting in the basic interpreter… this badge sounds great!

把它握在手中是很特别的，但是软件才是让它活起来的东西。Voja 最初的想法是一个有基本翻译的徽章，但我们有更多的东西。我们在微芯片论坛上找到了他关于基本 PIC 的一个非常老的帖子，我们联系了[jaro mir su kuba](https://hackaday.io/jaromir)——他在 Hackaday.io 上很出名，是今年早些时候硬币电池挑战赛的[冠军。Jaromir 同意加入并为这个项目编写软件。请花时间为此感谢 Jaromir，它已经变成了一个巨大的项目！](https://hackaday.com/2018/01/15/coin-cell-hacks-that-won-the-coin-cell-challenge/)

[![](img/ef0e790335b7e3688b377355ba7a5426.png)](https://hackaday.com/wp-content/uploads/2018/05/dsc_0869.jpg) 对于那些希望在复古计算体验中保持纯净的人来说，Jaromir 有几样东西适合你。值得注意的是，badge 在 Z80 仿真器上运行 CP/M。CP/M 是 Z80 老式计算机上非常流行的操作系统，为了验证这个系统，我们一直在运行 Zork！但这当然不仅限于游戏。徽章作为 CP/M 的 ROM 驱动器，包括 xmodem。使用 USB 转 TTL 串行电缆，您可以将程序传输到使用闪存芯片进行存储的三个 512 kB 驱动器中的一个上。当然你也可以在徽章之间转移徽章。

还有一个巨大的倒退是以不变的形式运行的微小的基本的副本。这不是徽章上的主要 BASIC 解释器，但是可以追溯到 1970 年代，挑战自己用准系统解释器做一些真正有趣的事情是很有趣的。对于那些想要重温的人，[这里有一本可以追溯到 1979 年的小小的基础手册](http://www.ittybittycomputers.com/IttyBitty/TinyBasic/TBuserMan.htm)。

徽章上的主要事件是 Hackaday BASIC 解释器，该解释器已被定制为充分利用所有徽章功能。它能够从 16 个存储插槽中保存和加载程序，但它也可以通过串行将程序传输到徽章上或从徽章上传输下来。它使用简单的脚本语言驱动徽章上的音乐。有用于控制 led 的文字，旋转引脚头上的 GPIO，通过改变颜色、移动光标、控制屏幕刷新和使用扩展的 ASCII 字符集来更直接地控制显示器。你可以通过访问[这个库](https://github.com/Hack-a-Day/basic-badge)来检查你自己的软件。

 [![Random colors of Hackaday](img/7e95648d7388737ee2f411f4efc75c99.png "belgrade-badge-basic-color-demo")](https://hackaday.com/2018/05/15/retro-computer-badge-for-hackaday-belgrade-has-everything-you-wished-for-back-in-the-day/belgrade-badge-basic-color-demo/) Random colors of Hackaday [![Simple code](img/4a0c0b2ca0eb4b1b3ec88b98b739c661.png "DSC_0871")](https://hackaday.com/2018/05/15/retro-computer-badge-for-hackaday-belgrade-has-everything-you-wished-for-back-in-the-day/dsc_0871/) Simple code

所有这些确实使它成为你手中的复古电脑。我迫不及待地想看到数以百计的这些被打印出来，并给一个充满硬件极客的会议带来欢乐！

## 难以置信的场景

徽章破解仪式将在午夜举行，给每个人大约 14 个小时的时间用徽章做一些特别的事情。我们希望看到所有级别的黑客，从从未编程使 led 闪烁的人，到演示场景的老手用他们的定制代码吹走股票固件。

现在就开始构思你的黑客吧。如果你有，带上 USB 转串行线和/或 PIC 编程器(我们手头会有一些，但越多越好)。有最佳音乐、最佳演示、最佳基础、最佳 CP/M 和一些其他类别的奖项。但让这变得有趣的不是奖项，而是向真正欣赏你创造力的人展示你的创造力。这些是你的人，你需要去贝尔格莱德。

[买票](https://www.eventbrite.com/e/hackaday-belgrade-2018-tickets-42286732756?aff=hadcom0515)来和我们一起创造一些回忆吧！