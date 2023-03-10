# 糖果机给你出了个谜语

> 原文：<https://hackaday.com/2016/03/08/candy-dispenser-riddles-you-this/>

不久前，有人给 AdaCore 送来了糖果机。过了一段时间，[杨奇煜-乔托]受到挑战，要让它变得更有趣。所以他决定[让人们更难收到糖果](https://hackaday.io/project/9989-candy-dispenser-with-a-twist)——你知道，鼓励知识增长——并阻止人们过量食用美味的食物。

分配器本身非常简单。它包括一个装有糖果的漏斗，一个带蜗轮的马达，用于输送所述糖果，以及一个小型红外传感器，当你在下面挥手时(为了接收那些甜甜的糖果)，该传感器会进行检测。

他决定让系统按原样运行，只中断与电机馈电的连接。这样，当你在下面挥手时，你必须在继续之前回答一个技能测试问题…

[杨奇煜]使用 STM32F469 发现板添加了一个触摸屏，以创建一个关于 AdaCore 或 LadyAda 的随机问题生成器，以确保他们渴望糖果的员工一直在听。如果你答错了，就不给你糖果！但是没有什么能阻止你再次尝试…

 [https://www.youtube.com/embed/n077RFpqTaE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/n077RFpqTaE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



如果他想更进一步，总会有我们去年万圣节推出的[糖果或死亡机器](http://hackaday.com/2014/10/30/push-button-receive-candy-or-death/)…