# 用太阳能电池板想象邻居

> 原文：<https://hackaday.com/2018/01/05/imaging-the-neighborhood-with-solar-panels/>

像许多家里有太阳能装置的人一样，[耶鲁安·博耶]很想知道他的电池板到底输出了多少能量。但与大多数人不同的是，他是一名数据科学家，对编程有着浓厚的热情，对可视化有着非凡的天赋。在他最新的博客文章中，[耶鲁安]详细描述了他解释一些异常数据的努力是如何以发现[他的太阳能电池阵列实际上充当了一台分辨率极低的相机](https://www.jeroenboeye.com/blog/solar-panel-analysis-pt-3-scanning-for-objects/)而告终的。

这一切都是从他注意到在某些月份，他的电池板产生的能量没有遵循预期的曲线开始的。一般来说，固定太阳能电池板的能量输出应该遵循一条清晰的钟形曲线:增加输出，直到太阳处于理想位置，然后随着太阳远离而减少输出。自然云量会对此产生影响，但是云量应该来来去去，而不是在数据中重复出现。

[![](img/79cd2cc31aefe64b403f7790366d3e05.png)](https://hackaday.com/wp-content/uploads/2018/01/pvimg_detail1.png)

Expected versus actual power output.

[耶鲁安]最终意识到发电量下降是因为他院子里的两棵大树。这让他有了一个想法，看看他是否可以把他的太阳能电池板变成一个简单的相机。理论上，如果他在任何给定时间比较面板的实际和预期输出，结果可以用作图像中的“像素”。

他首先创建了一个全年太阳能电池板理想能量输出的模型，不仅考虑了诸如太阳高度变化等显而易见的变量，还考虑了大气扩散造成的能量损失。然后，将这个模型与他的太阳能电池板的实际功率输出进行比较，低效率的时期被标为较暗的点来表示障碍。最后，绘制的数据被放置在从太阳能电池板的角度拍摄的全景图像上。果不其然，太阳能电池板效率低的时期与太阳能电池板视野内的树木和建筑相对应。

我们已经见过很多太阳能黑客了，但这一次肯定是第一次。[通常人们更担心效率最大化](https://hackaday.com/2015/03/17/solar-charge-controller-improves-efficiency-of-solar-panels/)或[与他们一起追踪太阳](https://hackaday.com/2013/07/21/hardware-store-goods-and-an-mbed-combine-help-solar-panels-track-the-sun/)。