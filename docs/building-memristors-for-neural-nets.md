# 为神经网络构建忆阻器

> 原文：<https://hackaday.com/2015/11/03/building-memristors-for-neural-nets/>

今天可用的大多数电子元件只是几年前可用元件的改进版本。微控制器变得更快，内存变得更大，传感器变得更小，但我们已经多年甚至几十年没有看到真正新颖的组件了。没有比忆阻器更有趣的电子元件了，它们的新应用[现在已经可以从 Knowm 商业获得](http://knowm.org/knowm-memristor-capable-of-bi-directional-learning-press-release/)，Knowm 是一家处于将机器学习直接应用到硅上的前沿公司。

数字电路的全部意义在于以一系列 1 和 0 的形式存储信息。忆阻器也可以存储信息，但是是以完全模拟的方式。每个忆阻器都会根据通过它的电流改变自己的电阻；“写入”正电压会降低电阻，“写入”负电压会使器件回到高阻态。

![Cross section of the metal chalcogenide memristor. Source: Knowm.org](img/55c8e93f8ac76362d0c26c5f2cf97ca1.png)

Cross section of the metal chalcogenide memristor. Source: Knowm.org

这种新的忆阻器基于博伊西州立大学(Boise State University)的 Kris Campbell 博士]所做的研究，这位研究人员负责我们今年早些时候看到的银硫族化物忆阻器。像这些早期的设备一样，已知的忆阻器是使用硫族化银分子构建的。为了降低忆阻器的电阻，正电压将银离子“拉入”金属硫族化物层。银离子留在硫族化物层中，直到施加负电压将它们“推”回来。这赋予了忆阻器的核心功能——能够记住有多少电流流过它。

这项技术不同于惠普在 2008 年制造的第一批忆阻器[，并允许 Knowm 以相对较高的产量在硅上制造功能性忆阻器。Knowm 目前正在](http://www.nature.com/nature/journal/v453/n7191/full/nature06932.html)[销售一种“tier 3”忆阻器部件](http://knowm.org/product/tier-3-bs-af-w-memristors/)，这种部件只有八分之二的设备没有通过 QC 测试。八个忆阻器都工作的“第一层”部件售价为 220 美元。

至于这种忆阻器的应用，Knowm 正在使用这项技术，他们称之为热力学 RAM，或 kT-RAM。这是一个小型协处理器，允许比更传统架构的计算机更快的机器学习。这种 kT-RAM 采用二叉树布局，忆阻器充当节点之间的链接。

虽然现在说 kT-RAM 处理器在现实生活中执行机器学习任务是否会更好或更有效还为时过早，但机器学习协处理器确实有点像 80 年代人工智能复兴期间开发的机器学习芯片。30 年前，芯片上的神经网络是由波士顿附近的几家公司创建的，直到有人意识到这些神经网络可以在台式 PC 上更有效地模拟。不过，kT-RAM 有点新颖，高度并行，有了新的电子元件，它可能正是将机器学习直接推向硅所需要的。

[https://player.vimeo.com/video/135505624](https://player.vimeo.com/video/135505624)