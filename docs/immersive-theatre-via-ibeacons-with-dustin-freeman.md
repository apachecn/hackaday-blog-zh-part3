# 达斯汀·弗里曼通过 IBeacons 的沉浸式剧院

> 原文：<https://hackaday.com/2015/12/18/immersive-theatre-via-ibeacons-with-dustin-freeman/>

结合数学和戏剧背景，[ [达斯汀·弗里曼](http://dustinfreeman.org) ]致力于沉浸式互动戏剧体验。白天【达斯汀】是[枕骨](http://occipital.com/)的空间交互工程师，他制作[结构传感器](http://structure.io/)。在业余时间，达斯汀致力于数字剧院项目，让观众远离传统的一排座位。

沉浸式剧院的概念类似于“逃离房间”挑战，选择自己的冒险经历，因为参与者通过根据提供给他们的信息做出决定来控制体验的结果。[达斯汀]在他的演讲中解释说，试图打破《逃离房间挑战》中存在的时钟的感觉在 ***泛光灯的《画*** 中没有帮助。泛光灯是一家戏剧制作公司，*这幅画*是圣何塞州立大学表演教授 [Joshua Marx](http://j-marx.com/) 和 2015 年[hack aday 超级大会](http://hackaday.io/superconference)演讲人【Dustin Freeman】共同打造的沉浸式戏剧体验。

 [https://www.youtube.com/embed/il426KYu88g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/il426KYu88g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



## 这幅画

沉浸式互动剧院体验需要参与者与环境互动的物理空间。为了满足这个要求,[Dustin]得以进入一家白天关门的酒吧。周期性的访问要求沉浸式影院的设置能够快速完成。[Dustin]和[Josh]能够在 30 分钟内完成这项工作。没有什么比拥有一个真实的场景更好的了，而*地下酒吧*是一个功能齐全的酒吧，只需最少的准备就可以与角色互动。

*绘画*的前提是你到达*地下酒吧*，【乔希】在门口迎接你让你进去。你进去时，他解释说他很忙，需要你上楼去给他拿一幅画。你配备了一部智能手机和一副耳机，以便[Josh]可以与你交流。

## 科技导航 [![ibeacon_map](img/3a39c8c8a00558ce1aaac821c1478a47.png)](https://hackaday.com/wp-content/uploads/2015/12/ibeacon_map.png)

整个布景中的道具包括 iBeacons。当智能手机检测到 iBeacon 时，会收到两条信息:iBeacon ID 和智能手机到 I beacon 的距离。这些参数需要一些创造性的代码，不仅仅是为了推进故事，也是为了解码接收到的信息。来自感测的 iBeacon 的数据是标量而不是向量，接收多个标量提出了一系列必须小心解决的问题。如下图所示，距离智能手机相同距离的两个 iBeacons 有量子物理位置。上图展示了[Dustin]如何通过改变每个 iBeacon 的活动半径来解决距离问题。

[![ibeacon_scalar](img/b1c98ebe793d52a1e9203d0e5882a79f.png)](https://hackaday.com/wp-content/uploads/2015/12/ibeacon_scalar.png)

为了确定故事将如何展开，达斯汀使用了[绿野仙踪技术](https://en.wikipedia.org/wiki/Wizard_of_Oz_experiment)来勾勒出所需的代码。通过由[乔希]扮演向导来模拟场景，[达斯汀]将沿着打印出的*地下酒吧*平面图移动一个游戏棋子。这个例程被削减为 4 个变量，这两个变量可以变成基于 iBeacon 位置信息的脚本导航。

## 现实世界的问题

在设计产品的技术方面时，出现了一些小问题。大多数男人(至少是参与设计这幅画的两个人)把手机放在裤子前面的口袋里。这并不是对每个人都适用，女装通常没有口袋，相当多的人选择后口袋来装手机。这显然会将传感器的几何形状更改为 iBeacons，从而影响脚本事件的触发时间。在后口袋或背包中，电话可能无法进入触发事件的物品的正确范围内。这个问题还没有解决，但可能会通过一种特殊的衣服来解决，每个参与者都可以穿上这种衣服来规范手机口袋的位置。

这是蓝牙技术的一个有趣的应用，[Dustin]做了一个信息丰富的演讲，不仅包括什么有效，还包括什么失败以及失败的方式/原因。在视频和幻灯片中，[Dustin]提出了一些很好的发人深省的问题，如果您对以类似方式使用 iBeacon 技术感兴趣，这些问题将是继续这项工作的好地方。