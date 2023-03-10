# 对于游戏动画，神经网络比人类走得更好

> 原文：<https://hackaday.com/2017/05/05/game-characters-move-better-with-neural-networks/>

现代电子游戏已经走过了漫长的道路，从水管工马里奥在屏幕上跳来跳去。当今游戏中难以置信的复杂环境是吸引新玩家的一部分，这种体验是通过角色与场景的互动来实现的。然而，虚拟世界的幻觉被表演动作中人物的不自然运动所破坏，例如突然转身或爬山。

为了补救突然的动作，丹尼尔·霍尔登等人。al]最近[发表了一篇论文](http://theorangeduck.com/media/uploads/other_stuff/phasefunction.pdf) (PDF)和一段视频，展示了一种大大改进实时角色控制机制的方法。所提出的系统使用神经网络，该神经网络已经使用在各种地形上行走、跳跃和其他序列的大型数据集进行了训练。关键是将两足动物运动的过程及其循环行为分解为一系列子步骤或阶段。每个阶段都转化为角色移动时的自然姿势。系统离线预计算下一阶段，以节省运行时的计算资源。然后考虑用户控制、角色的先前姿态(包括关节位置)和地形几何，计算动画的后续帧。该计算由回归网络完成，该网络计算关节的未来位置，混合函数用于运动匹配，如[Simon Clavet]的[演示文稿](http://twvideo01.ubm-us.net/o1/vault/gdc2016/Presentations/Clavet_Simon_MotionMatching.pdf)(PDF)和[视频](https://www.youtube.com/watch?v=4pdcA3mhe0E)中所述。

这种方法在诸如崎岖地形和障碍物的环境中证明是有效的，这些环境涉及在遵循用户指示的同时进行诸如规避、攀爬、跳跃或迈步的交互。最终结果是一个非常真实的渲染，计算成本非常低，如下图所示。它的应用超越了游戏，一直延伸到增强现实和虚拟现实领域。

神经网络最近很热门，随着谷歌的张量流项目进入 DIY 机器人，这标志着编程的新时代即将到来。

 [https://www.youtube.com/embed/Ul0Gilv5wvY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Ul0Gilv5wvY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

