# 本周失败(1996 年):70 亿美元溢出

> 原文：<https://hackaday.com/2016/06/30/fail-of-the-week-in-1996-the-7-billion-dollar-overflow/>

那是 1996 年，欧洲航天局准备在太空中争夺商业霸权。他们的新型阿丽亚娜 5 号火箭可以将两颗三吨重的卫星发射到太空。它比以前的任何东西都更有力量。

火箭在火焰柱上升向天空，携带四颗非常昂贵且没有保险的卫星。37 秒后它自毁了。70 亿美元的 RUD 雨点般落在南美洲圭亚那航天中心附近的海滩上。休息之后是发射失败的视频。

造成这一切的原因是一点代码中的一个不正确的类型转换，它甚至不应该在实际启动时运行。谈谈失败。

有两位代码。一个测量横向速度，一个用于导航系统。测量端使用 64 位变量，而制导端使用 16 位变量。这个代码是从一个更早的更慢的火箭借用的，它的速度永远不会大到超过 16 位。然而，阿丽亚娜 5 号可以用一首蠢朋克歌曲来描述，并很快超过了这个值。

导致溢出的代码实际上是一个调整火箭的预发射软件。它应该在火箭发射前关闭，但由于火箭发射经常被推迟，工程师们在发射 40 秒后暂停，这样他们就不必一直重启它。

ESA 从不责怪任何一个承包商。程序员做了假设。工程师们制定了合理的捷径来使他们的工作更容易。它已经通过了检查、批准，最后是发射活动。

他们肯定从这次事件中吸取了教训；从那时起，阿丽亚娜 5 号火箭已经成功完成了 86 次任务中的 82 次。在 2023 年退役之前，它至少还有五次发射合同，用于现在正在开发的阿丽亚娜 6 火箭。这一事件也改变了关键软件和冗余系统的测试方式，第一次让公众注意到代码失败的危险。

如果你想了解更多，Reddit 上有一个[大讨论](https://www.reddit.com/r/programming/comments/4nv66p/assumptions_are_bad_when_a_single_6416_bit_cast/)向我们提示了这次失败，一篇相当彻底的[维基百科文章](https://en.wikipedia.org/wiki/Cluster_(spacecraft)#Launch_failure)，刊登在《纽约时报》上的原始文章在这里有所反映[。](https://around.com/ariane.html)

 [https://www.youtube.com/embed/qnHn8W1Em6E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/qnHn8W1Em6E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



* * *

《一周失败》是一个黑客专栏，它把庆祝失败作为一种学习工具。通过写下你自己的失败和[给我们发送一个故事的链接](mailto:tips@hackaday.com?Subject=[Fail of the Week])——或者发送你在互联网旅行中发现的失败报道的链接，帮助保持乐趣。