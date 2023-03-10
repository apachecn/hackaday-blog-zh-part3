# 阿尔瓦罗·彼尔托的激光射击机器人

> 原文：<https://hackaday.com/2015/12/04/alvaro-prietos-laser-shooting-robots/>

阿尔瓦罗·彼尔托在超级电脑展上的演讲以一张幻灯片开始，幻灯片提出了一个反问:“为什么是激光射击机器人？”反问句需要答案吗？[阿尔瓦罗]给出了一个答案:“因为激光很棒。”我们同意。

但 DEFCON 举办激光机器人比赛给你一个借口也无妨。你看，[阿尔瓦罗]的激光机器人是 2014 年 DEFCONBOTS 竞赛的第一名，2015 年，一个更具雄心的设计获得了第三名。他的超级演讲都是关于他一路走来学到的东西，因为这就是这些比赛的重点，对吗？

## “我不知道我在做什么。”

[阿尔瓦罗]以免责声明开始，但当[阿尔瓦罗]说他不知道自己在做什么时，他的意思是他没有接受过建造激光操纵、自主炮塔机器人的正式培训。(我们在学校是怎么错过那节课的？)

[![iterations](img/3e304140515d8181436260453c8ad57e.png)](https://hackaday.com/wp-content/uploads/2015/12/iterations.jpg)

不过，他是一个真正的黑客；他开始的时候不知道自己在做什么，但他还是开始了。[Alvaro]的带领我们从第一个原型开始，他使用了角度分辨率不足的伺服电机，安装在他(显然)用手用刀切割的轻木框架上，通过带有定制传动装置和步进电机的激光切割框架，一直到他的 DEFCONBOTS 2015 参赛作品，基于 [OpenBeam](http://www.openbeamusa.com/) 铝挤压件，并使用专业的激光显示 [galvos](https://en.wikipedia.org/wiki/Galvanometer) 能够以每秒数千个点的速度摆动光束。

## 经验教训

[![IMG_2593-110](img/706a64db27573bf40587e1b94eddc952.png)](https://hackaday.com/wp-content/uploads/2015/12/img_2593-110-e1449168408232.jpg) 由于【Alvaro】是一个“以写代码为生”的电气工程师，所以他根本就没怎么关注代码这方面。相反，他分享了许多他通过设计和制造真实的物理机器人来瞄准和照亮移动的乒乓球所学到的东西，包括:

*   业余爱好伺服电机不是非常准确
*   激光切割机可以定制齿轮，但你必须测量东西
*   微步并不总是出现
*   使用摩擦驱动时，公差非常重要
*   如果你的机器人转弯并有电线，它需要限位开关
*   网络摄像头摇摆不定，难以安装
*   把所有东西都做成两个一组，然后把它们都带到比赛中，因为东西会坏掉
*   事先彻底测试一切
*   在敏感的模拟电路中使用几个 trimpots，电阻有容差
*   在计算机视觉代码中，首先找到你感兴趣的区域，然后只详细分析该部分
*   需要 3V 的激光变成 3V 以上的暗发光二极管

还有更多。但不要相信我们的话，你自己去看一下[阿尔瓦罗]的讲话。

 [https://www.youtube.com/embed/qSHjzEO5CiE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/qSHjzEO5CiE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



最后，如果你对计算机视觉感兴趣，爱好机器人，甚至对激光节目感兴趣，你真的应该看看[【阿尔瓦罗】的个人网站](http://alvarop.com/)和 [DEFCONbots 2015 参考机器人](https://github.com/Defconbots/2015_Reference_Robot)。在这两个地方，你都可以找到模板、代码和经验，了解哪些对人们有用，哪些没用。如果你受到启发，也许你会在明年夏天和阿尔瓦罗较量一番。