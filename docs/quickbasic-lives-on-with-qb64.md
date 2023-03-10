# QB64 延续了 QuickBASIC

> 原文：<https://hackaday.com/2018/02/22/quickbasic-lives-on-with-qb64/>

当我得到我的第一台电脑，一台运行 MS-DOS 6.22 的二手 386 时，我没有互联网连接。但我确实安装了 QuickBASIC，还有当地图书馆扔掉的一堆编程杂志，所以我有很多事情要忙。当时，我认为 QuickBASIC 和 magic 几乎没有什么区别。我可以编写简单的代码并编译成。exe，把它放在软盘上，交给其他人在他们自己的机器上运行。这似乎好得难以置信，这种技术怎么可能改进呢？

[![](img/e719027b991be42e2c1ff21a4fe74250.png)](https://hackaday.com/wp-content/uploads/2018/02/qb64_msdos2.png) 当然，那是很多年前的事了，和现在的情况大不相同。当今的编程语言*比 80 年代和 90 年代的单调乏味的基本变体更有能力。但是，当我发现一张软盘里装满了我几十年前写的程序时，我不禁想让它们再次运行起来。有了像 DOSBox 这样的东西，我想我应该能够安装 QuickBASIC IDE 并运行它们，就像我回到我可信赖的 386 上一样。*

 *不幸的是，情况并非如此。也许我对 DOSBox 不够精通，但我无法让 IDE 实际运行我从软盘上下载的任何源代码。这是令人失望的，但我突然想到，现代 BASIC 解释程序可能正在互联网的某个角落开发，也许我可以找到一种方法来运行我将近 30 年前的代码，而不必依赖 30 年前的软件。

## QB64 项目

[![](img/0d5f3f29bae33849580afbf9cb09c9a8.png)](https://hackaday.com/wp-content/uploads/2018/02/qb64_logo1.png) 四处找了一下，[找到了 QB64 项目](https://www.qb64.org)。这是一个开源的 QuickBASIC 开发环境，不仅与现有程序完全兼容，还增加了在 my 386 上无法想象的功能和能力。显示 PNG、加载 TTF 字体或在后台播放 MP3 都可以通过一两个命令来完成。

这样的事情在最初的 QuickBASIC 中是可能的，但是更多的是存在于技术演示领域。哦，我早就可以用这样的软件做游戏了！我不得不满足于哔哔声和滴滴答答的声音，即使这样也需要你自己去计算音调的时间。

更好的是，QB64 是跨平台的，支持编译成 Linux、Windows 和 Mac OS 的本地二进制文件。这意味着我不仅可以在 IDE 中运行我的旧代码，还可以将它编译成 Linux 桌面的二进制文件。我不再拥有 Windows 电脑，但有了 WINE，我可以运行 QB64 的 Windows 版本，并编译一个。exe，我可以把它送给那些还生活在黑暗时代的朋友们。

你甚至可以使用 QB64 将 QuickBasic 代码编译成 Android 应用程序，尽管有相当多的障碍需要跳过，而且它目前只在 Windows 上运行。

## 召唤黑魔法

对于那些从未在老式机器上编写过 BASIC 代码的人来说，这可能是个迷，但是下面的代码创建了一个 800×600 的屏幕，全屏播放 PNG，播放 MP3，并使用 TrueType 字体编写消息。

```
' Init screen
SCREEN _NEWIMAGE(800, 600, 32)

' Load files
menubg& = _LOADIMAGE("splash.png")
menufont& = _LOADFONT("font.ttf", 30)
theme& = _SNDOPEN("theme.mp3", "SYNC,VOL")

' Set theme volume, start playing
_SNDVOL theme&, 0.3
_SNDPLAY theme&

' Load font
_FONT menufont&

' Show full screen image
_PUTIMAGE (0, 0), menubg&

' Say hello
PRINT "Hello Hackaday!"
```

作为比较，[这个简单显示 JPEG 图像的 QuickBasic 工具](https://dmitrybrant.com/1999/04/16/a-jpeg-viewer-for-qbasic)记录了 653 行代码。

## 重访项目

在我十几岁的时候，我创作了一个“ [Drugwars](https://en.wikipedia.org/wiki/Drugwars) ”风格游戏的图形版本。你在一个像素化的环境中移动一个小棍子人，买卖我在电影中听说过但从未见过的物质。太可怕了。但这是我年轻时的一部分，我想如果我能用 QB64 把一些现代的 flash 硬塞进去会很有趣。

事实证明，透明的 png 和显示适当字体的能力使事情变得容易得多。能够在后台播放音乐和环境声音效果使得即使是草率完成的游戏看起来也要好得多。以下截图是我的少年犯罪幻想主菜单，QB64 应用前后。请注意，核心源代码本身或多或少是相同的，我只是将它与加载和显示外部文件的能力交错在一起。

 [![qb64_dw](img/c4457705100c0d4983dd95ff1977f14e.png "qb64_dw")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/02/qb64_dw.png?ssl=1)  [![qb64_dwr](img/b3be05cc0202b88c4fcdcc533491c955.png "qb64_dwr")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/02/qb64_dwr.png?ssl=1) 

## 你应该使用 QuickBasic 吗？

不，你绝对不应该。我写这篇文章并不是为了试图说服任何人去学习一门在我们的许多读者出生之前就已经达到顶峰的编程语言。QuickBASIC 是一种过时的语言，其过时的方法和局限性让现代程序员感到困惑。但是对于我们这些初学这门语言的人来说，QB64 确实在使这门经典语言现代化方面做得非常出色，即使只是在大格局中相对较小的程度上。

能够将我在 90 年代初在 DOS 386 上编写的基本代码磁盘转换成 2018 年的 Linux 二进制文件是一项非常出色的成就，我向 QB64 开发团队致敬，他们使这成为可能。我不会用这种语言写任何新的代码，我也不建议你这么做，但能够重温我生活中的这段时期并[将它带进现代时代](https://hackaday.com/2017/07/05/fixing-bugs-in-ancient-basic-games/)是一件非常有趣的事情。*