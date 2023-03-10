# 你车库的喷水器

> 原文：<https://hackaday.com/2016/09/12/wazer-the-waterjet-for-your-garage/>

大多数业余爱好者的车库里没有喷水器，但如果可以的话，他们会的！水射流(或水射流切割机)是一个了不起的工具。只需在 x-y 扫描架上安装一股高压砂砾和水流，压力就会产生足够的侵蚀力，几乎可以穿透任何薄材料。不幸的是，声称你自己的喷水会侵蚀掉你的钱包一个很大的洞。到目前为止，机器的起价约为 7.5 万美元，更不用说它们会占用你在两个车库中的大部分工作空间。

我们大多数日常黑客想玩这个工具的好处，把他们的零件送到专业商店。因此，我们不经常听说日常黑客使用水射流，或水射流切割零件，但有一个例外。早在 2014 年，一群来自宾夕法尼亚大学的学生建造了一个功能性喷水器，零件清单显示价格约为 5000 美元。现在同一支队伍回来了。这一次，他们不仅仅是一次性的，而是一个功能齐全的产品，名为 [Wazer](http://wazer.com/) ，几分钟前刚刚在[推出了 Kickstarter 活动](https://www.kickstarter.com/projects/1294137530/the-first-desktop-waterjet-cutter)，已经将 10 万美元的目标翻了两番。它是怎么做到的？全套服务的起价在 3599 美元到 4499 美元之间。毕竟，这是众筹，但 20 倍的降价是一个强大的动力。

## 第一眼；最初的想法

在过去的一周里，我和 Wazer 的工作人员进行了一次现场演示，所以我想我应该简单介绍一下我的想法。首先，让我们先了解一些技术细节:

*   全封闭切割床
*   工作区:12 英寸。x 18 英寸。
*   精度为 0.003 英寸。精度因材料而异。
*   切割速度各不相同，但典型值如下所示:
    *   1/8 英寸。铝:每分钟 1.8 英寸
    *   1/8 英寸。不锈钢:每分钟 0.7 英寸
    *   1/8 英寸。玻璃:每分钟 11.8 英寸
*   最大材料厚度各不相同。这里有一个快速分类:
    *   低碳钢:3/16 英寸。
    *   铝 1/4 英寸。
    *   玻璃 3/8 英寸。

首先，值得一提的是，与传统水射流相比，Wazer 的尺寸、厚度和切割速度有限。然而，它并不局限于其广泛的材料范围。也就是说，我们并不指望那些想为车库添置一台这样的车的人会把这款工具视为 10 万美元车型的替代产品。相反，这是一种接触切割各种薄而平的材料的新方法，其公差足以构建符合机器限制的功能原型。

## 最低系统要求

正如我们可能预期的那样，Wazer 不会在一些温和的设置之前就开始从盒子中切割零件。首先，Wazer 需要一个主供水管道的入口水源和一个出口水源。如果你想把这个庞然大物安装在客厅打印机旁边，那就算了吧，当然，除非你的房子也安装了相应的管道。除此之外，喷水器实际上足够小，足够独立，能够在室内运行……也就是说:如果你愿意在清理之前在你的房子周围挥舞一些沙子。总而言之，这种工具的目的是在车库或车间着陆，它产生的水需求和潮湿部分可能会让它留在那里。

![28993754294_1c75fc8f58_z](img/7d79e866c40ff23eb52febb330c38994.png)

总的来说，这个设备是非常完备的。磨料石榴石是一种现成的商品，可以从侧面的抽屉中装入。水流和磨料石榴石在喷嘴处混合，外壳保持机器内部的混乱。最后，高压系统是由一个小的外部盒子提供的，在他们的宣传视频中，这个盒子藏在机器下面。

除了你的水费，还有两个消耗品需要记住。首先是石榴石，用后需要折腾；第二个是聚乙烯床，它最终会因反复切割而磨损。

## 维护和操作:

从设计到切割与激光切割机界面有许多相似之处。只需导入一个矢量图形，将切割位置定位在 x-y 网格“激光切割机样式”上，即可选择切割位置。还有一个额外的选项来选择沿着线的哪一侧(或死点)追踪。

![29585034506_80d96dba3b_z](img/72a6dd9a84a81cbc06ab548789977619.png)

石榴石被过滤到前面不连续的“收集容器”中(这是为了避免下水道堵塞)。检查使用过的石榴石的数量只需拉出容器，取出后将水排出，并扔掉沙子。Wazer 实际上很好地解决了维护问题。一个训练有素的专业人员可能会用传统的喷水器从机器中舀出沙子几分钟，这个系统让用户带着几箱沙子快速前往垃圾桶。

![29619537585_1ba9f9c3c5_z](img/3606f016bd7e8ae383f58c59d77574b1.png)

固定工件也相当简单。Wazer 船员已经取得了一些相当坚实的成功，只需直接拧入波纹聚乙烯的支持。零件上的力(1)与铣床相比相当温和，并且(2)大部分是向下的，因此零件不需要复杂的装配系统来固定它们。切割时，只需几个螺钉(如右图所示)就可以防止盘子蠕动。

## 一流的陈列柜

人们很容易忘记，大多数为下班后的工程师开发工具的人实际上并不是冷酷的销售人员。他们也是工程师——他们也不例外，都是热爱好的副业项目的人。在 Hax Accelerator 办公室，我预览了一些他们已经使用他们现在提供给我们的工具构建的附带项目。

 [![29585086886_575bf8519f_z](img/e5f983ce8ec271b47de20a300c50b087.png "29585086886_575bf8519f_z")](https://hackaday.com/2016/09/12/wazer-the-waterjet-for-your-garage/29585086886_575bf8519f_z/)  [![28995785723_78bb601df1_z](img/def740d59ba39763f2eefa43cc3ab86f.png "28995785723_78bb601df1_z")](https://hackaday.com/2016/09/12/wazer-the-waterjet-for-your-garage/28995785723_78bb601df1_z/)  [![29619513625_dab467f113_z](img/d1f57cf8a8b050bf09b0dd73d466afc4.png "29619513625_dab467f113_z")](https://hackaday.com/2016/09/12/wazer-the-waterjet-for-your-garage/29619513625_dab467f113_z/) 

与激光切割机相比，喷水器在适用材料方面的限制要少得多。上面的刀把是从 D2 工具钢上切下来的，然后由专业的刀匠完成。在中间，四轴飞行器的框架是由 FR4 和碳纤维切割而成的(升级版 PCB-copter，我们将让你就在这里存在！).

假定工具的有效直径只有大约 1.5 密耳(0.0015 英寸)，那么可获得的细节水平很容易超过任何手工工匠的精细程度。另一个优点是用这种工具生产的零件具有一致的可重复性。想象在同一台机器上用相同的图案切割贴整面墙并不困难。

## 抓住新的可能性

随着商店里任何新机器的到来，人们很容易开始对各种可能性垂涎三尺。这种新的动物如何能增加我们已经熟知的切割和喷射技术的词汇呢？首先，值得一提的是，这里没有免费的午餐。与能够切割更厚材料的专业机器相比，这台机器的切割速度较慢。也就是说，如果你正在购买其中的一个，切割速度很可能不是立即拥有零件的限制因素。看看他们的精度，Wazer 也不能做同样的精密工作的一个体面的数控轧机。然而，在大多数情况下，它不需要！对于那些不担心压配合和滑动配合的普通人来说，0.003 密耳已经足够了。

对于严肃的机械师来说，0.003 密耳并不算大，但这并不妨碍交易。机械加工和制造行业的人们经常铸造一些复杂零件的粗略形状，然后在铣床上完成重要的实际尺寸。同样，对于需要更严格公差的零件，Wazer 可以成为“第一遍”机器，从许多薄材料中进行粗切——甚至是一些否则会威胁到日常爱好机械师的材料，如 FR4 或工具钢。对于重要的尺寸，人们可以将他们的零件放到另一台机器上来完成重要的尺寸。也许孔的尺寸需要用合适的铰刀扩大到最终尺寸，或者也许一些边缘的表面光洁度需要用精加工端铣刀磨光。总而言之，Wazer 在切割其他难以切割的材料时应该没有问题。

通常情况下，想要对零件进行喷水的严肃爱好者会将他们的设计送到专业喷水机构。不幸的是，如果时间对我们不利，运输和其他人的项目阵容都可能会推迟。如果设计中有错误，或者一旦我们开始在家里组装它，如果我们发现 *Rev-1.0* 有一些设计问题，我们就会被一个可以避免的问题推迟:零件需要时间才能回来。

Wazer 不是没有耐心的人的工具。这是一种新的方式来完善我们对如何使用喷水部件的理解。后期设计，在我们回到办公桌组装零件之前，只需要半个小时左右。当然，错误会耗费我们的材料，但是没有一种学习机制能比迭代速度和即时反馈的综合效益更好。

此外，附近的喷水器可以将注定要成为垃圾的零件重新放回你的原材料货架上。如果你一直在用 G10 或碳纤维制造四轴飞行器，为什么不把那块报废的主板从电子垃圾堆里拿出来，从那里切割下一个框架呢？还记得那些你很快意识到没有呼吸器就不能加工的玻璃纤维板吗？立刻把它们从垃圾桶里拿出来。最后，看看你周围被扔掉或在当地旧货店出售的垃圾。那个饼干纸？没错。玻璃窗？绝对的。陶瓷盘子？为什么不呢？欢迎来到一个全新的骑自行车的世界。

就在几年前，一个团队带着他们的概念证明登陆了这些页面，我们很高兴一次性产品已经开始成熟为一个启动的商业产品，可以让成千上万渴望的学生，家酿机械师和工匠等。请记住，任何 Kickstarter 机器的第一次更新都有其缺陷，一台价值 10 万美元的 4K 水车永远无法完成与它的 10 万美元的兄弟姐妹相同的工作。尽管如此，我们还是很高兴社区能够体验到 3D 打印机之外的制作，我们热切地等待着他们的回应。

 [https://www.youtube.com/embed/P9d8l09Rqoc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/P9d8l09Rqoc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

