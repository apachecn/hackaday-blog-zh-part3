# 翻转你的桌面来启动 Linux

> 原文：<https://hackaday.com/2016/02/01/flip-your-desktop-over-to-boot-linux/>

[Andy France]将他的电脑[组装成一个 Windows XP 盒子](http://www.mini-itx.com/projects/windowsxpbox/?page=4)。(没错，这是以前的。)他大部分时间都需要运行 windows，但偶尔启动一下 Linux 也不错。这就是问题所在。如果他在他的 Windows XP 电脑上运行 Linux，他会被取笑的。唯一的解决办法是为他的电脑做一个 Linux 的套子。每当他运行 Linux 的时候，他都会把袖子套在箱子上，从他飘忽的眼神中掩饰自己的羞愧。一旦他的计划完全成型，他就更进一步，修改了电脑，这样如果袖子戴上了，它就会自动启动 Linux，如果袖子没戴上，它就会启动 Windows。

只有当电脑上下颠倒时，Linux 的保护套才能滑动。所以他需要检测它什么时候处于这种状态。为此，他将一个开关连接到电脑的一个 com 端口，并将其连接到机箱顶部。他修改了 MBR 中的汇编代码来读取交换机的状态。当 Linux 套筒打开时(因此计算机翻转过来)，它引导 Linux。当袖子脱掉时，窗户。干净利落。将一台小型电脑放在一个立方体中，用这个技巧让它启动不同的操作系统会很酷。或者可能是一台计算机在一个方向上启动到来宾模式，而在另一个方向上启动整个系统。

[via [黑客新闻](https://news.ycombinator.com/item?id=11009558)