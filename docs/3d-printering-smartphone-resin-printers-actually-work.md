# 3D 打印:智能手机树脂打印机实际工作

> 原文：<https://hackaday.com/2016/11/18/3d-printering-smartphone-resin-printers-actually-work/>

去年春天，世界目睹了一些惊人的事情。这是一款能够彻底改变地球、拯救世界、将你的智能手机变成 3D 打印机的设备。众所周知，Kickstarters 不会卖空自己。当然，我说的是[的 OLO 3D 打印机](https://www.kickstarter.com/projects/olo3d/olo-the-first-ever-smartphone-3d-printer/)，后来更名为[的小野 3D 打印机](http://www.ono3d.net/)，表面上是因为商标纠纷。

虽然基于细丝的 3D 打印机非常强大，切片软件也越来越好，但基于树脂的打印机能够打印出几乎无与伦比的质量。如果你想要高分辨率的物体和精细的细节，树脂打印机是一个不错的选择。然而，这些树脂打印机比传统的细丝打印机要贵一些。几百美元可以买到一台好用的 i3 克隆机，不到 1000 美元就能买到一台真正的能打印四种颜色的 Prusa。顶级的桌面树脂打印机，来自 [Form Labs](https://formlabs.com/) 的 Form 2，起价 3500 美元。


小野(或 OLO)改变了这一切。这款 99 美元的树脂打印机没有使用激光、电流计或 DLP 投影仪，而是使用智能手机显示屏将光线照射到一桶树脂上。根据 OLO Kickstarter 的支持者的说法，这太棒了。一个白痴科技博客称，这是“3D 打印技术民主化的福音”。更理智的人质疑由手机驱动的树脂打印机的可行性。

对于更熟悉 3D 打印机的人来说，有几个关于 ONO 的问题。Kickstarter 活动展示了储存在半透明瓶子中的光敏树脂。控制这台打印机的 Z 轴阶段显然是通过耳机端口。不同型号的智能手机有不同的厚度，没有文件记录这会如何影响树脂罐到屏幕的距离。如果在 OLO 上打印一张照片需要一个小时，你就不能用手机一个小时。OLO(或小野)在今年的纽约世界创客大会上有一个展位，我没有看到这些机器实际工作。简单来说，我们不知道小野实际上是否有效。对于一台在 Kickstarter 上首次亮相的 3D 打印机来说，这并不奇怪。

然而，仅仅因为 Kickstarter 活动没有任何意义，几个月前才交付给支持者，9 月份显然没有工作模式，并不意味着技术有任何问题。使用 LCD 将光线直接照射到树脂罐底部的想法很有趣，至少值得做一些实验。

[终于有人做到了](https://www.youtube.com/watch?v=uybLNu0zv28)。在本周上传的 YouTube 视频中，[Ionel Ciobanuc]展示了一台家酿 3D 打印机，这与小野假装的很像。这是一个 5 英寸的液晶显示器，由运行 [nanoDLP](http://www.nanodlp.com/) 的树莓 Pi 驱动，带有一个简单的电动 Z 轴，将印刷物从树脂中拉出。它工作了。与 Form Labs 打印，甚至是基于细丝的机器的高质量打印相比，它工作得不是很好*，但是它工作了。无论如何，这是一个实验和概念验证。*

 *ONO 是否有效，以及何时发货都无关紧要。我们已经看到更酷的打印机和更有趣的技术[失败的壮观](http://hackaday.com/2016/05/11/peachy-printer-collapses-investor-built-a-house-instead-of-a-printer/)。在任何情况下，树脂打印机暂时都将是怪异和奇特的设备，由激光和电流计或昂贵的 DLP 投影仪驱动。

然而，这个来自[Ionel]的实验性 3D 打印机展示了即使是最少的 BOM 也能做什么。认为这项树脂打印实验的建造成本不到 100 美元并不是不合理的，进一步的实验可以将成本降得更低。ONO 打印机提出的想法——在树脂罐底部放置显示器——实际上是可行的。*