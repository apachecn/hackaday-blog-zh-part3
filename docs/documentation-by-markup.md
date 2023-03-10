# 通过标记的文档

> 原文：<https://hackaday.com/2017/01/18/documentation-by-markup/>

事情似乎循环往复。使用 TROFF 或 LaTeX 等老式工具编写文档就像知道一个秘密代码一样。可视化编辑器很快就取代了它，尽管即使是 WordStar 也有一些你作为文本输入的“点命令”。然后 HTML 出现了，我们又回到了文本字符串的编码格式。

快进到现在，HTML 的无处不在让这看起来很正常。当然，有可视化编辑器，但是现在为粗体文本编写**似乎是再正常不过了。然而，随着 HTML 处理越来越多的任务，它也变得越来越复杂。这导致了像 Markdown 这样的东西的产生，它只是用于简单的文本格式化。**

有时图片和图表对于记录复杂的软件和硬件是至关重要的。当然，有很多视觉方式来画画。 [Mermaid](http://knsv.github.io/mermaid/) 旨在将简单的文本标记引入到您的图形化图表创建中。像这样的图表:

[![](img/fff14950c5313203b7ca6d671ac26a70.png)](https://hackaday.com/wp-content/uploads/2017/01/mermaid.png)

这并没有展示美人鱼的所有能力，它继承了 [d3](https://d3js.org/) 。例如，您可以设置 CSS 样式，甚至允许 JavaScript 集成来使您的图具有交互性。另一方面，像菱形决策块这样的东西很难看起来正确。我们也不知道如何用一条线来连接两列。

## 代码内部

下面是该图的标记代码:

```
graph LR

 id1[Build Super Project]
 id2a{Project Working?}
 id3>Submit to Tip Line]
 id4[Wait for Hackaday post]
 id5((Prosper))
 id1-->id2a
 id2a-->|yes|id3
 id2a-->|no|id1
 id3-->id4
 id4-->id5

```

## 关于代码

“graph LR”线告诉 Mermaid 图形从左到右。接下来的几行定义了所有的块。您可以看到文本周围的字符给出了节点的形状。即“()”做一个圆角框，“())”做一个圆。

带有“–>”的线定义了节点之间的连接。你可以在网上找到关于[语法的完整参考。](http://knsv.github.io/mermaid/#flowcharts-basic-syntax)

## 只是流程图？

该系统目前可以制作流程图、序列图和甘特图。文档非常好，你可以把它嵌入到网页中。你也可以使用[在线编辑器 live](http://knsv.github.io/mermaid/live_editor/) 并生成链接或 SVG 文件。

有许多方法可以将可编辑的标记图放入文档中。例如，我们已经介绍了 [XWave 和另一种时序图字体](https://hackaday.com/2015/05/25/need-timing-diagrams-try-wavedrom/)，其中字体直接形成时序图。对于更现代的东西，有[波隆](http://hackaday.com/2015/05/25/need-timing-diagrams-try-wavedrom/)。美人鱼看起来像是这些工具的一个很好的补充，但是对于流程图来说。

文档并不总是项目中最有趣的部分。但是，如果你想让其他人复制它，记录你的成就，甚至在你完成一个系统多年后，当你不得不修复或扩充它时，回忆细节，你需要好的文档。美人鱼可能只是一个工具，可以帮助你敲出一个好看的图表，这是值得一千字。