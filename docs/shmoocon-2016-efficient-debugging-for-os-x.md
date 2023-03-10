# shmoocon 2016:OS X 高效调试

> 原文：<https://hackaday.com/2016/01/19/shmoocon-2016-efficient-debugging-for-os-x/>

开发人员热爱他们的 MAC 电脑，如果你看看它附带的软件，就很容易明白为什么。OS X 是一个非常强大的 Unix-ey 环境，通常基于非常强大的硬件。OS X 有一个巨大的、难以置信的缺点:调试器糟透了。GDB，其他平台的标准，没有 OS X 和苹果的替代品，LLDB 非常糟糕。在 Safari one 崩溃太多次后，[ [Brandon Edwards](https://twitter.com/drraid) ]和[ [Tyler Bohan](https://twitter.com/1blankwall1) ]决定他们需要自己的调试器，所以他们建造了一个，[并在上周末的 Shmoocon 上展示了他们的工作。](https://github.com/blankwall/MacDBG)

构建一个合适的工具始于对现有工具的调查，在确定 GDB 显然不可安装并且 LLDB 很糟糕之后，他们的 lit 审查转向了更深奥的问题。[钻头切片机就是他们降落在](https://github.com/zorgiepoo/Bit-Slicer)上的东西。这是一个“游戏训练器”或允许人们修改记忆的东西。它有点像调试器，但不是真的。 [VDB 是另一个选择](https://github.com/zdevito/vdb)，但这又是粗糙的边缘，并没有真正的工作。

当前 OS X 调试器的问题是，调试器使用的工具并不存在。 [ptrace 被阉割](http://uninformed.org/index.cgi?v=4&a=3&p=14)，OS X El Capitan 中的系统完整性保护引入了 *root* 无法写入的保护位置。如果你有最新的 Mac，祝你在/Applications 中修改任何东西都好运。

为了得到一个易于使用、易于脚本化的调试器，[Brandon]和[Tyler]决定编写他们自己的调试器。他们最终编写了他们见过的唯一一个围绕 [kqueue](https://www.freebsd.org/cgi/man.cgi?query=kqueue&sektion=2) 而不是 ptrace 构建的调试器。这允许调试器对被调试的进程是非侵入性的，注入代码，并一次附加到多个进程。

对于那些一直茫然地盯着“GDB 在哪里”这一大堆答案的人来说，这是一件大事。[Brandon]和[Tyler]已经开始为一台非常好的机器准备一个非常好的工具。