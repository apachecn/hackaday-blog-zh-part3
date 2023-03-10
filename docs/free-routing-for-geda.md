# 免费前往 GEDA

> 原文：<https://hackaday.com/2017/02/08/free-routing-for-geda/>

如果你使用软件来设计 PC 板，很可能你对自动布线器有自己的看法。有些人不会使用不能自动路由跟踪的包。其他人不会接受一个机器布局，当他们可以用手做他们自己的时候。当然，你可以将两者结合起来，很多设计师都这样做了。

开源的 gEDA PCB 包(和 pcb-md)有一个自动路由器，但是它非常简单。[VK5HSE]展示了如何[使用一些工具](https://vk5hse.blogspot.com.au/2017/02/automatic-routing-in-geda-pcb-and-pcb.html)与 Java [Freerouting](http://www.freerouting.net/) 应用程序交互，以获得更好的结果。例如，最初的路由器制作了方形拐角，而如果配置正确，Freerouting 应用程序将创建角度和圆弧。

这些工具使用行业标准的输入和输出格式来交换文件中的数据。然而，在格式和使用的测量单位方面存在一些细微的差异，因此[VK5HSE]必须对 pcb-md 的滤波器代码进行一些更改。但是，下一个版本将原生包含这些代码。

[布莱恩]一直试图在所有东西中制造[多氯联苯。虽然[VK5HSE]的帖子是关于 pcb-md 的，但他学到的东西可能对其他布局程序也有用。当然，有些人](https://hackaday.com/2016/09/21/creating-a-pcb-in-everything-introduction/)[永远不会接受](https://hackaday.com/2016/08/11/hackaday-prize-entry-autorouters-are-for-the-weak/)自动路由。