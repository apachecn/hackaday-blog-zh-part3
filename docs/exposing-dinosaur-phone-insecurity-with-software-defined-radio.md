# 通过软件无线电揭露恐龙手机的不安全性

> 原文：<https://hackaday.com/2017/06/05/exposing-dinosaur-phone-insecurity-with-software-defined-radio/>

早在每个人都有一两部智能手机之前，电话的实现比今天要奇怪得多。大多数电话都有真正的物理按钮。更奇怪的是，这些手机通过*物理线路*与其他手机相连。很奇怪，对吧？这些被称为“座机”，三、四年前，这项技术摆脱了这种致命的束缚。

事情变得更奇怪了。有些手机是无线的，就像你的智能手机一样，但是由于某种原因，它们在离你家几百英尺的地方收不到信号。这些是“无绳电话”。[腐蚀剂]几年来一直致力于解构这些无绳电话背后的安全性[，发现这些无绳电话根本不安全](https://www.youtube.com/watch?v=LCQtgizdgGU)。

此漏洞所涉及的电话是来自 Vtech 的标准 5.8 GHz 无绳电话。传统观点认为这些电话相当安全——至少比八九十年代的无绳电话安全——因为很少有人身边有双工微波收发器。HackRF 就是那个，只要 300 美元。这最终是注定要发生的。

这实际上只是对这些无绳电话内部无线电系统的探索。在对一部无绳电话进行黑客攻击后，[腐蚀剂]发现这部电话从技术上讲并不工作在 5.8 GHz 频段。控制信号，例如将手机与基站配对，发生在 900 MHz。在这里，一个简单的重放攻击就足以让手机响铃。更糟糕的是:只要用 HackRF 看看 5.8 GHz 频段，[腐蚀者]就能在手机打开时发现一个调频语音频道。没错:这部手机传输你的声音没有任何加密。

这不是第一次发现无绳电话完全缺乏安全性。不久前，他还在探索 DECT 6.0 标准，这是一种针对 PBX 和 VOIP 的欧洲无绳电话标准。这里也没有保安。如果座机还存在的话，那将会令人不寒而栗。

 [https://www.youtube.com/embed/LCQtgizdgGU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LCQtgizdgGU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/omS7OMLAnaA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/omS7OMLAnaA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

