# 从零到纳米

> 原文：<https://hackaday.com/2017/02/22/from-zero-to-nano/>

你有没有想过从零开始打造自己的 Arduino？[Pratik Makwana]分享了[设计、构建和刷新 Arduino Nano 克隆](http://www.instructables.com/id/Make-Your-Own-Arduino-Nano-DIY-Arduino-Nano/?ALLSTEPS)的整个过程。这不是一个入门级的项目，需要一些焊接知识才能成功使用如此小的元件，但这是非常值得的。虽然这是一个廉价的建设，它可能更便宜，只是买一个纳米。这不是重点。

这里的目标和这个项目有趣的部分是，你可以跟踪制作板子的整个过程。你可以用这些知识来设计你自己的电路板，你自己的变体，甚至一个完全不同的项目。

![from-zero-to-nano-thumb](img/78e3f1df1457cd59c9ff0a17d01dcc12.png)【Pratik mak wana】从展示如何在 EDA 工具(Eagle)中设计电路原理图以及相应的 PCB 版图设计开始。然后，他使用墨粉转移方法和层压机将电路压印到铜板上，以便稍后进行蚀刻和钻孔。具有挑战性的焊接过程并不详细，如果你需要一些焊接 SMD 尺寸元件的帮助，我们之前介绍过一些不同的过程，从[烤面包机](http://hackaday.com/2012/03/08/toaster-oven-reflow-soldering-roundup/)到[用 Kapton 胶带](https://hackaday.com/2011/04/03/kapton-tape-aids-in-drag-soldering-surface-mount-parts/)拖拉焊接过程。

最后但并非最不重要的，引导加载程序固件。这是使用 Arduino UNO 作为主设备，新创建的 Arduino Nano 克隆作为目标设备来完成的。之后你就可以走了。要运行实际的草图，只需使用标准的 USB 转 UART 转换器刻录草图，然后照常运行。

瞧，从零到纳米:

 [https://www.youtube.com/embed/Gu7Na6rlPP4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Gu7Na6rlPP4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



如果你仍然想构建一个 Arduino，但是难度对你来说有点高，也许一个好主意是从虾开始。