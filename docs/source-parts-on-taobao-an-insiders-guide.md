# 淘宝上的源部件:内部人员指南

> 原文：<https://hackaday.com/2017/03/28/source-parts-on-taobao-an-insiders-guide/>

对于硬件爱好者和制造商来说，去深圳华强北已经成为一种朝圣之旅。虽然华强北是一个巨大的、仍然活跃的资源，但越来越多的中国和外国硬件开发商都在淘宝上采购组件。可供选择的范围要大得多，而且本地购买的送货时间很少超过 48 小时，通常不到 24 小时，这非常适合深圳硬件生态系统的高速发展。

对于海外买家来说，虽然淘宝的费用与全球速卖通和中国的网上商店相当，或者略低，但选择的范围是后者的很多很多倍。学习如何有效地从淘宝上采购零件既有趣又有力量。

[![](img/82ce0d4daa853a2f43269eb1e6e13b3c.png)](https://xkcd.com/1133/)

XKCD: [Up Goer Five](https://xkcd.com/1133/)

### 理解中文是如何工作的是有帮助的

如果你知道它的中文名字，你几乎可以在淘宝上找到任何东西。这并不意味着你需要说中文，但你应该明白它是如何工作的。虽然该网站可以使用谷歌翻译导航，但它不能接受英语搜索。因此，弄清楚一个物体或部件在中文里叫什么是第一个也是最大的挑战。一旦你找到了那串字符，你就不需要能够读懂它，就像任何其他代码片段都不需要可读就能被操作一样。只要你大致知道代码代表什么，这就是你所需要的。

在 Bunnie Huang 的 *[深市电子必备指南](https://www.crowdsupply.com/sutajio-kosagi/the-essential-guide-to-electronics-in-shenzhen)* (没错，就是([绝对必备](https://hackaday.com/2016/02/07/bunnies-guide-to-shenzhen-electronics/))中，Bunnie 把中文比作 XKCD 的 *[Up Goer Five](https://xkcd.com/1133/)* 。这期漫画用“人们最常用的 1000 个单词”来解释火箭的所有部件。这是一个非常准确的类比，一旦不会说中文的人掌握了这一点，他们就能够在网上采购时更准确地定义他们的搜索词。几千个单词用来描述大量的组件。如果你把它分解，通常会很直观。

A 电脑(Diànnǎo)，英文直接翻译为“电子大脑”或计算机。虽然大多数汉字已经偏离了它们的起源，变得不可辨认电(Diàn)或“电动”是一个你会看到很多。这个角色表现了一朵带着闪电的云落到了地上。同样，一个手机“手机”是一种移动电话，并且手看起来还是有点像手上的手指。

如果你记住这种结构——中文零件名称很少是一个专用词，更多的是一组半直观的关键字——它会使查找这些名称容易得多。

### 通过名称查找您的零件

有些部分你可以简单地使用谷歌翻译，但有时它不够具体或返回该词的错误上下文。在这种情况下，最好使用已经本地化为中文的技术网站作为资源。

![](img/5c5b65e3f4f37dfe08b291c7c284ce48.png)

对于电子零件。com 和。Mouser 网站的 cn 版本可以互换。大多数情况下，只有类别名称被翻译，但这可以让你非常接近，并有助于与中国工程师合作。你可以把你想要的零件类型的网址发给他们，有图无混淆。他们可以对说英语的人做同样的事情，但是反过来。

所以:

```
http://www.mouser.com/Sensors/Capacitive-Touch-Sensors/_/N-1b8oy/
```

成为

```
http://www.mouser.cn/Sensors/Capacitive-Touch-Sensors/_/N-1b8oy/
```

对于机械零件，Misumi 通过将“us”替换为“cn”来提供类似的功能。

```
https://us.misumi-ec.com/vona2/mech/M1500000000/M1501000000/M1501030000/M1501030100/
```

成为

```
http://cn.misumi-ec.com/vona2/mech/M1500000000/M1501000000/M1501030000/M1501030100/
```

### 细化您的搜索

谷歌翻译“开关”会让你”开关“你可以把它粘贴到淘宝搜索栏，得到一个大的、有点随机的、主要是交流电灯开关的集合。但是如果我们做了绳子"开关 DPDT“事情开始变得更有用了。如有可能，添加电压、安培数等数字。必要的，它会让你更接近。

![](img/aa465ff8a59bcaaf26337dfb8615d43f.png)

如果我们看到非常接近我们想要的东西，我们有两个选择，第一个是鼠标悬停在产品图像上。将出现一个橙色条，它可能会让您选择“找相似”或“找到相似的”。点击这个会显示与该产品相近但不相同的东西。

如果没有“查找相似”的选项，你可以将中文描述复制到谷歌翻译中，找到更多有用的关键词。

6-pin DPDT blue MINI small SMTS-202 double-pole double-pass toggle switch YW2-102

谷歌翻译告诉我们字符串“双刀双通钮子开关“是‘双刀双钮开关’。使用该字符串进行搜索会得到大量类似的开关供我们选择。

### 通过图像找到您的零件

![](img/414567b9a194e74b207df72a8de8dfd2.png)

淘宝有一个非常聪明的按图片搜索功能。如果你有你想要的零件的图片，你可以用它来搜索。它是搜索栏右侧的小相机图标。

这有许多用途:找到产品的上游经销商，找到产品的未经授权的副本，以及查看新的众筹活动是否基于预先存在的中国产品。

### 点菜

与亚马逊不同，淘宝上的“购买”按钮更多的是邀请与店主聊天购买。通常会有一定量的必要对话。一些不会说中文的人复制并粘贴了一个“对不起，我不会说中文”的样板，但许多商店不会基于此履行订单，因为他们担心沟通失误会导致差评，这将使他们付出的代价超过该商品的利润。

超过一半的订单都是通过聊天完成的，缺乏直接的购物车和购买流程，这意味着那些不懂中文的人很难在淘宝上购物。他们也不接受贝宝，虽然应该有一个接受西方信用卡的过程，但我不知道有谁成功设置了这个过程。

幸运的是，有一些服务可以帮你解决这个问题。你给他们发送你想要的产品的链接，收取适当的费用，他们会处理剩下的事情。这些经纪人购买物品，用你的 PayPal 或信用卡支付，代表你接受包裹，合并它们，然后转发给你。通常，物品的价格加上服务费仍然低于通过全球速卖通购买同样的物品，并且给你更多的选择。

部分淘宝经纪人(排名不分先后):

*   [https://www.bhiner.com](https://www.bhiner.com)
*   [https://www.taobaoring.com](https://www.taobaoring.com)
*   [http://www.yoybuy.com/en/](http://www.yoybuy.com/en/)

在深圳时，Ringy 通过微信提供免费翻译服务，并可以将包裹送到您的酒店。

*   微信:ringyringy

### 要避免的事情

“星期一之前能准备好吗”

永远不要问它是否会在特定日期前准备好，答案几乎总是“是的”。如果不是这样，你也无能为力，所以他们没有理由失去这次销售。所以当和你的淘宝经纪人打交道时，不要问“他们能在周一前准备好吗？”，而是问“他们说哪一天会准备好？”你会得到更准确的答案。

一般来说，在中国采购时应遵循这一模式。问“它有什么颜色？”在更成问题的“他们能做粉红色的吗？”。当在供应商既定的时间表和产品范围内工作时，比从新事物开始要容易得多。

“你要它做什么？”

千万不要回答店家的这个问题。这意味着他们想知道是否可以根据 imagine 能满足您的需求的东西来替换其他东西。为什么 3D 打印机加热床需要昂贵的 PEI 床单？亚克力应该没问题。你会得到一张非常漂亮的 PEI 彩色亚克力板，价格比 PEI 便宜一点，但比亚克力板贵很多。坚持使用 BOM 上列出的项目，如果他们不知道它的用途，会有更大的替换失败和差评的风险。

避免购买任何未经其他买家审核的商品。

他们的评论是假的吗？当然，有很多(尽管越来越好了)。但是店主购买它们是要花钱的，通常也有真品——这是包含在列表中的成本。如果一个列表没有反馈，如果你(或代表你的代理)给它一个差评，店主只要把它撤下来就不会有任何损失。

### 不要讨价还价

当你选择使用淘宝而不是西方的分销商时,“让它更便宜”的部分已经完成了。进一步试图省钱会导致问题。淘宝上的每个人都来自相同的工厂，如果一个相同或非常相似的产品便宜得多，那是有原因的。看看前五个最受欢迎的部分上市，这些或更高的平均价格是你可以预期支付。

虽然在淘宝上采购肯定存在挑战，但对于任何硬件爱好者来说，大量的、经常可定制的选择使其成为非常有用的资源和技能集，以备不时之需。

* * *

Naomi Wu 是一名硬件爱好者，深圳人。上述指南是在深圳五金社区的大力协助下编写的。