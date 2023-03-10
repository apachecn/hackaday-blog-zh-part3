# 气动旋转叶片接头伸出温柔的援助之手

> 原文：<https://hackaday.com/2017/05/03/pneumatic-rotary-vane-joints-lend-a-gentle-helping-hand/>

Festo 发布了一段视频，展示了他们的 BionicCobot(T1)的工作情况，这是一种气动机器人手臂，旨在帮助工作站上的人类。因为它与人类密切相关，所以它必须是安全的，不会产生有害的运动，并且在遇到障碍时做出反应，例如含有脆弱人类骨骼的手臂。这是通过气动和旋转叶片实现的。

![Rotary vane in action](img/a7feefb4a7cd76fcc1208c67710c7ee7.png)

Rotary vane in action

手臂有七个自由度，三个在肩部，一个在肘部，另一个在下臂，两个在手腕。但你找不到任何电动马达或齿轮。相反，每个都包含一个旋转叶片。压缩空气推动叶片的两侧。如果叶片两侧的气压相同，那么叶片就不会旋转。但是一边的压力比另一边大，叶片就会旋转。这很像人类手臂，两块肌肉一起弯曲手臂，一块肌肉收缩，另一块放松。他们一起被称为[对立的一对](https://en.wikipedia.org/wiki/Anatomical_terms_of_muscle#Agonists_and_antagonists)。此外，每个关节具有电路板，该电路板具有用于监控关节的两个压力传感器。

使用气动技术，如果遇到障碍，压力可以释放，使其立即安全。并且空气是可压缩的，接头可以像弹簧一样工作，进一步增加了安全性。通过控制压力，弹簧可以变得更紧或更松。

你可以在休息时间下面的视频中看到它的运行，以及更多细节，如他们如何使用 [ROS，流行的开放系统机器人操作系统](http://hackaday.com/2014/01/29/the-robot-operating-system-ros-101/)，我们在之前已经在这里见过[很多次，以及他们的 Festo 阀组，其中一个我们自己的【James Hobson】用于](http://hackaday.com/?s=robot+operating+system)[他光滑的极乐世界外骨骼](http://hackaday.com/2014/08/30/homemade-superhero-james-diy-exoskeleton/)。该视频还涵盖了他们如何处理运行软管，运动学和用户界面软件。

 [https://www.youtube.com/embed/tD501C2v0jM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/tD501C2v0jM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

