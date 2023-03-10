# 微控制器负荷计告诉你它目前的工作强度

> 原文：<https://hackaday.com/2017/05/13/microcontroller-load-meter-tells-you-how-hard-its-currently-working/>

为嵌入式应用程序编写代码可能很困难。你可能会遇到各种各样的问题——竞争条件、冲突的外围设备、意外的程序流——任何这些都会对你的项目造成破坏。有一件事可能会把事情搞砸，那就是如果你的微控制器卡在一个例程上，没有正确的调试硬件和软件，这可能很难发现。 [[Terry]为此开发了一款微控制器负载测量仪。](http://128.199.141.78/instrument-mcu.html)

这是一个简单的设置——微控制器上一个名为 *loadmeter-task* 的程序向一个机械安培计发送一串脉冲。当芯片空载时，用微调电位器调节电流表，使其读数为“0”。当其他任务偷取 CPU 时间时，*负荷计任务*发送脉冲的时间就少了，因此负荷计向左倾斜。

总的来说，这是一段快速简单的代码，你可以用一个备用的 GPIO 引脚添加到任何项目中，这可能有助于你进行调试。另外，知道你的项目对芯片的推动有多大也很酷。

如果你想知道更多关于你的芯片在做什么，看看这篇关于[在线调试](http://hackaday.com/2011/08/01/making-the-case-for-in-circuit-debugging-tools/)的有用性的文章，或者阅读一下[比尔·赫德关于 ICE 和 OBD-II 的实验](http://hackaday.com/2017/05/09/obd-speed-pulse-part-2-behold-the-ice/)。