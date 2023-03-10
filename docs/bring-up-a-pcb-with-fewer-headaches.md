# 带来一个更少麻烦的 PCB

> 原文：<https://hackaday.com/2018/01/10/bring-up-a-pcb-with-fewer-headaches/>

当 fab house 的一套新电路板送到你家门口时，你做的第一件事是什么？涂焊膏，填充元件，然后把它放在回流焊炉里？这是做这件事的一种方法。但是在工厂里，很多不明显的事情也会出错，比如短路和未钻孔的过孔。一个小小的错误可能意味着几个小时的沮丧和理智的质疑，因为你正在解决一些现在被锡膏和 0603 掩盖的问题。

在 IO 上，[Bhavesh]试图将这些问题扼杀在萌芽状态，用[一个全面的和解释性的指南来正确地提出 PCB](https://hackaday.io/project/29189-how-to-bring-up-a-pcb) 。尽管它是基于 fab house 板的，但这个一应俱全的计划适用于任何项目，从套件构建到定制条形板电路。当新电路板到达时，[Bhavesh]会进行几项连续性检查，并用显微镜进行目视检查。对于条形板布局，最好验证切割走线之间没有连续性。他继续讨论焊膏，触及正确的处理和存储、应用和问题纠正。

本指南中我们最喜欢的部分是组件表。做这些是一个很好的预防措施，就像在你烤蛋糕之前把你所有的配料都放在柜台上一样。如果你知道你需要什么，为什么不准备好呢？[Bhavesh]为每种组件类型使用一张表格，按升序列出所有相关值，并在旁边展示组件卷轴。

该指南还包括锡膏——他的模板晚到了，所以该指南涉及手工涂抹锡膏。他提出了一个组装电路板的计划，从一个角落开始，一圈一圈地工作，先放置小元件。接下来是回流以及所有重要的回流后检查，在魔法消失之前检查桥接和不良连接。

发现错误的最佳时间是在你将订单发送到工厂之前的*。 [Hackaday 自己的【约书亚·瓦斯奎兹】已经把你报道得够多了](https://hackaday.com/2017/05/10/designing-for-fab-a-heads-up-before-designing-pcbs-for-professional-assembly/)。*