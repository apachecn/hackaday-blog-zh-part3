# Bash 中的软件开发

> 原文：<https://hackaday.com/2018/02/27/software-development-in-bash/>

真正好的想法往往适用于所有情况。这句话是“永远不要带着剪刀跑”，而不是“除非你正要去隔壁房间，否则不要带着剪刀跑。”软件开发方法是一个好主意，我们大多数人都有自己的工具选择。但是，如果您正在开发大量 bash 或类似的脚本，该怎么办呢？因为 bash 不是一种“真正的”编程语言，就应该即兴发挥吗？[奥斯卡]说[不](https://oscarforner.com/2018/02/24/Software_development_using_Bash)，如果你写的剧本超过两三行，我们同意。

我们之前已经论证过 [bash 是一种编程语言](https://hackaday.com/2017/07/21/linux-fu-better-bash-scripting/)(你们中的许多人不同意)。也许不是最棒的，当然也不是最性感的，但是 bash 在某些类型的系统上几乎无处不在，对于许多任务来说是非常高效的。[Oscar]展示了他如何使用源代码格式化程序、linter 和单元测试框架来使 bash 脚本符合现代软件开发。我们很确定他也使用了源代码控制，但是这看起来很简单，以至于它不会出现在他在 GitHub 中的库的链接之外。

棉绒尤其重要(顺便说一下，我们在之前已经[讨论过了)。由于 bash 是解释的，所以很难在运行时之前捕捉到所有错误。如果你关心的话，它还能捕捉到可移植性问题。我们也对单元测试框架印象深刻，因为这将支持测试驱动的开发，这是非常高效的。](https://hackaday.com/2017/03/29/lint-for-shell-scripters/)

下一步？[写一个游戏](https://hackaday.com/2013/02/05/bash-games/)。或者使用 bash 来[抓取网站数据](https://hackaday.com/2010/12/25/crash-course-in-html-manipulation-from-a-shell-script/)。