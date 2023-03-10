# 从 XP 到 10，DoubleAgent Pwns 你所有的窗口？

> 原文：<https://hackaday.com/2017/03/22/from-xp-to-10-doubleagent-pwns-all-your-windows/>

Cybellum 团队发布了一种新的 0 天技术，用于在目标计算机上注入代码并保持持久性，命名为 [DoubleAgent](http://cybellum.com/doubleagentzero-day-code-injection-and-persistence-technique/) 。这项技术使用了自 XP 以来的所有 Windows 版本都提供的一个功能，该功能允许为任何可执行文件安装应用程序验证程序提供程序 DLL。验证者提供者 DLL 只是一个加载到进程中的 DLL，应该负责为应用程序执行运行时验证。然而，它的内部行为可以是攻击者想要的任何行为，因为他可以自己提供 DLL。

微软将其描述为:

> 应用程序验证器是用于非托管代码的运行时验证工具。Application Verifier 帮助开发人员快速发现细微的编程错误，这些错误在正常的应用程序测试中很难识别。在 Visual Studio 中使用 Application Verifier，通过识别由堆损坏、不正确的句柄和临界区使用引起的错误，可以更容易地创建可靠的应用程序。(…)

代码注入发生在受害者进程初始化的极早期，使攻击者能够完全控制进程，并且进程无法实际检测到发生了什么。一旦某个 DLL 被注册为某个进程的验证程序提供程序 DLL，每当该进程启动时，即使在重新启动、更新、重新安装或修补之后，它也会被 Windows 加载程序永久地注入到该进程中。

所以 Windows 的一切都结束了，对吗？嗯…不。问题是，要注册这个 DLL，注册的进程必须有管理员权限，这样它才能将正确的键写入 Windows 注册表。没有这些权限，这种攻击就无法进行。你知道，那种允许你为所有用户安装软件或者格式化你自己的硬盘的权限。因此，尽管这种技术有其优点，并且可能对绝对必须保持其完整性的进程提出挑战(如 Cybellum 团队在反病毒软件案例中指出的)，但必须首先出现一些其他安全缺陷，以便您可以注册这种“调试 DLL”。

如果你已经有管理员权限，你可以做你想做的事情，包括 DLL 注入来欺骗反病毒软件。(尽管禁用或删除它可能更容易。)这个新工具的优点是隐身，但是需要 root 的 0-day 是 0-day 吗？

[via [黑客新闻](http://thehackernews.com/2017/03/hacking-windows-dll-injection.html)