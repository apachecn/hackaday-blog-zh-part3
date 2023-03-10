# 通过逆向工程实现准确的咖啡账单

> 原文：<https://hackaday.com/2018/05/31/accurate-coffee-billing-through-reverse-engineering/>

如果你曾经在一个吝啬的办公室工作过，你会对公共咖啡壶很熟悉，它运行在某种荣誉系统的变体上。这里有一些纸，一个用胶带密封的破罐子，还有每六个月一次的例行通知，告诉人们不要为他们每天的啤酒付钱。这一切都有点过了。[谢天谢地，如果你和【Fabian】合作，这就不再是问题了(PDF 链接)。](http://www.comsys.ovgu.de/comsys_media/thesis/finished/BSc/2018_Fabian+Off+_+Reverse_engineering+a+DeLonghi+Coffee+Maker+to+precisely+bill+Coffee+Consumption-p-332.pdf)

该项目构成了[Fabian]论文的基础，论文中对德隆基咖啡机进行了逆向工程。这样做的明确目标是正确计量每种饮料所用的消耗品(咖啡豆)的量，以便根据用户选择的酿造品更公平地收费。这包括分解和理解咖啡机的内部通信，以及实现一个系统来记录和处理帐单。为了简单起见，[Fabian]决定使用他同事现有的计算机帐户来处理这个问题。轻松点。

这是一个高度学术的方法，我们确信这是一个非常刺激的项目，有许多美味的香气。毫无疑问，咖啡是黑客们的热门话题——[看看这个烘焙器，让你的游戏更上一层楼。](https://hackaday.com/2018/01/23/build-an-excellent-coffee-roaster-with-a-satisfyingly-low-price-tag/)