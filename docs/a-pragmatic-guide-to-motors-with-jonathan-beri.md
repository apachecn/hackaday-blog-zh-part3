# 乔纳森·贝里汽车实用指南

> 原文：<https://hackaday.com/2015/12/17/a-pragmatic-guide-to-motors-with-jonathan-beri/>

乔纳森·贝里(Jonathan Beri )是各种各样的制造商，对机器人、API 和开源有着浓厚的兴趣。白天，他致力于让 Android&iOS SDK 更容易使用，晚上，他会恳求 PID 控制器“已经开始工作了”最近，他参与了由 Maker Media 出版的《[Make:JavaScript Robotics](http://www.amazon.com/Jonathan-Beri/e/B00OMJ8Q1K/ref=dp_byline_cont_book_11)》(2015)。

[Jonathan]在 [2015 Hackaday 超级大会](http://hackaday.io/superconference)上的汽车演讲中涉及了很多内容。他讨论了有刷 DC，步进电机，伺服电机和无刷电机。虽然仅仅是对每种类型的电机的表面刮擦[Jonathan]触及了重要的细节，你可以用它来确定哪种类型的电机最适合你的项目。他整理的幻灯片为初学者提供了很多信息和提示，这些信息和提示在选择电机时可能会被忽略。例如，选择电机时应考虑的 30 个属性的列表。当[Jonathan]为他的一个项目选择发动机时，他会优先考虑这 7 个属性。休息过后，我们将对此进行更深入的探讨。

 [https://www.youtube.com/embed/vf7qHbEFYVw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/vf7qHbEFYVw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



## 控制![step-hrot](img/e0b9c773958b04a8c4d698fc8fd67726.png)

一旦你为你的项目确定了电机类型，真正的挑战就开始了，控制器。[乔纳森]做了一个出色的工作，为一个很少或没有运动控制经验的人展示了大图选项。在这一过程中，他提出了一些小建议，比如当你需要更多功率时，将 H 桥中的晶体管换成 MOSFETs，然后他会提醒你在增加功率时增加散热器，从而得到双倍的提示。我们知道[乔纳森]不能阻止你让魔法从你的 MOSFETs 中释放出来，但他正在努力尝试。

步进电机可能看起来更复杂，毕竟不像有刷 DC 电机有 2 根线连接到正电压和地面，步进电机可以有 4，5，6 或 8 根导线连接。[Jonathan]通过分析步进电机中到底发生了什么，在恐慌到来之前让我们冷静下来。步进机的线圈如何与他之前讨论过的 DC 马达相关联。此外，他用了几个例子来控制这些多线动物，并解释了为什么他使用一种技术而不是另一种。

[Jonathan]还提到他们可能会继续讨论闭环控制，所以请密切关注他的 hackaday.io 项目页面。休息之后，请观看视频，了解[Jonathan]对各种电机的概述，包括原理图控制器示例以及在哪里可以找到示例代码。

## 以身作则

我们想花点时间感谢[乔纳森·贝里]分享第一手技术演讲的经验。从概述他关于 hackaday.io 早期阶段的演讲的大致内容到[为他的演讲制作的幻灯片](https://docs.google.com/presentation/d/1oerI70z6QAJj2B7JoqPG69l8VsZmXnxlHWLvHEImL5w/edit#slide=id.gd3557fa9d_0_293)。[Jonathan]用他的谈话要点和来源评论了他的演示(比我们写的大多数代码都好),所以一定要注意寻找。你可以在观看上面的视频时点击他的演示，或者根据需要从项目中期的挫折中恢复过来。这就是说:最后一次感谢[Jonathan Beri]以如此开放和透明的方式分享他的流程，这是他应得的，我们希望将来能从[Jonathan]那里看到更多，我们也可能会让您参加闭环控制后续讲座；).

乔纳森可以在 [GitHub、](https://github.com/beriberikix) Twitter 上以 [@beriberikix](https://twitter.com/beriberikix) 的身份出现，在 Google+上以[+乔纳森贝里](https://plus.google.com/+JonathanBeri)的身份出现。