# 获奖后:Chipwhisperer

> 原文：<https://hackaday.com/2016/11/01/after-the-prize-chipwhisperer/>

离黑客日超级大会还有不到一周的时间，届时我们将宣布黑客日大奖的得主。Hackaday 奖是对 Hackaday 社区提供的最伟大的硬件的庆祝，在过去的三年里，我们一直在举办这个令人惊叹的比赛，我们已经看到了一些令人敬畏的东西。

虽然并不是每个参加 Hackaday 奖的项目都取得了成功——剪草机驱动的斩首杀手仍然被拴在它的测试台上——但在过去几年中，已经有一些引人注目的项目在工业、学术界和安全行业产生了不可思议的影响。在接下来的几天里，我们将重温这些项目，看看他们做得怎么样，看看他们对开源硬件世界的影响。

我们要看的第一个项目是由科林·奥弗林发明的工具[chip whisper](https://hackaday.io/project/956-chipwhisperer-security-research),用于查看芯片和固件的秘密内部，不管所述芯片上启用了什么嵌入式安全性。《ChipWhisperer》是第一届 Hackaday 奖[的参赛作品，获得了第二名](http://hackaday.com/2014/11/13/satnogs-wins-the-2014-hackaday-prize/)。从那时起，ChipWhisperer 已经成为事实上的硬件工具，用于调查时钟故障、侧信道分析和其他奇异的魔术，使安全分析变得如此有趣。

### 什么是芯片密语？

这个星球上的每个加密系统都有问题。Crypto 必须在真实的硬件上运行，随之而来的是分析总线、旁路攻击和时钟故障的能力。如果你在微控制器处理指令的时候让时钟出故障，某些事情*可能*会出错。如果你很优秀，你也许能收集到一点当时微控制器内部发生了什么的信息。

时钟故障、侧信道分析和芯片密语者袖子里的所有其他把戏已经存在了几十年。进行这些攻击和分析的设备非常昂贵。ChipWhisperer 是第一个支持这些攻击的低成本、开源工具链。ChipWhisperer 的低价和开源特性为研究、地下工程甚至一些硬件黑客在他们的工作台上修修补补打开了大门。

### 成功的例子

如果一个做时钟故障和功耗分析的设备有点太深奥，有许多关于 ChipWhisperer 的出版物和黑客可以作为一个真实、具体的例子。几个月前,[scanlime]决定从廉价的 Wacom 平板电脑上获得固件。这款平板电脑包括一个带有断开的调试引脚的处理器，但一切都无法访问；固件不能在线获得，试图从微控制器上下载固件是徒劳的。

芯片密语的出现解决了固件丢失的问题。通过将 Wacom 平板电脑上的晶体脱焊，并在设备启动时发送电源故障，微控制器将继续发送固件位。通过一点点分解和逆向工程，[scanlime]能够完全重建设备的固件:

 [https://www.youtube.com/embed/TeCQatNcF20?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/TeCQatNcF20?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



当然，从廉价的 Wacom 平板电脑上卸载固件并不是 ChipWhisperer 的唯一用途。两年来，ChipWhisperer 在学术界引起了很大的关注，发表了从 8 位 Atmel 微控制器上的 ECC 密码术到时钟故障安全平台的论文。

### 获奖后

第一届 Hackaday 奖的第二名只是 ChipWhisperer 的开始。从那以后，科林启动了 ChipWhisperer Lite，并投入大量资源为他的硬件开发了一个合适的软件栈。一个完整的社区围绕着 chip whisper 成长起来，大量的工作致力于重构 chip whisper 软件，将所有东西放入一个合理的架构中，并使开源项目的软件方面变得合理。

ChipWhisperer 是我们在 Hackaday Prize 中看到的最强大的工具之一。当然，执行这些功率故障和侧信道分析的设备以前就有，但是芯片密语是一种力量倍增器。以前，执行这些攻击的设备的成本相当于一辆汽车。ChipWhisperer Lite 仅售 300 美元左右。对于一个学者可以申请的任何资助来说，这已经足够便宜了。

当然，像所有好的项目一样，ChipWhisperer 还没有完成。科林正在研究 ChipWhisperer Pro，这是一个硬件版本，具有更大的 FPGA，用于更强大的实验。专业版还没有完全推出，但随着科林建立的社区，它肯定是一个非常强大的工具，并且仍然是我们在 Hackaday Prize 中见过的最好的项目之一。

The [HackadayPrize2016](https://hackaday.io/prize) is Sponsored by:[![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](https://hackaday.io/atmel) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://www.digikey.com/) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/)