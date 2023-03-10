# Nvidia 使用人工智能将标准视频转换为慢动作

> 原文：<https://hackaday.com/2018/06/25/nvidia-transforms-standard-video-into-slow-motion-using-ai/>

Nvidia 又回来了，推出了另一个应用机器学习的可怕演示:[人工将标准视频转换成慢动作](https://news.developer.nvidia.com/transforming-standard-video-into-slow-motion-with-ai/)——他们非常擅长展示人工智能的能力，以至于任何人都认为他们在试图为它出售硬件。

虽然大多数现代手机和相机都有慢动作录制的选项，但这通常是以牺牲分辨率为代价的，而且总是以牺牲存储空间为代价。要获得真正高的帧速率，你需要一台专业相机，而且在事件发生之前，你通常不知道应该用慢动作拍摄。如果我们可以在录制后将标准视频转换为慢动作，这不是很好吗？

这正是 Nvidia 所做的，[所有这些都很好地记录在一篇论文中](https://arxiv.org/abs/1712.00080)。在其核心，该算法必须采取两个帧，并人为地创建一个或多个帧之间。这不是插入帧的手动算法，这是一个完全成熟的深度学习系统。卷积神经网络(CNN)在超过 1000 个视频上进行训练——大约 30 万个单独的帧。![](img/92b359b70e2f9d723f9ad681eedc8471.png)

由于 CNN 的任何参数都不是时间相关的，因此可以根据需要生成任意多的中间帧，这是该解决方案与以前的方法不同的地方。在他们演示视频的一些镜头中，30fps 的视频被转换为 240fps 这需要为每对连续帧创建 7 个附加帧。

休息后的视频非常令人印象深刻，尽管如果你仔细看，你可以看到奇怪的缺陷，像曲棍球运动员的冰鞋或舞蹈演员的手臂。深度学习既是一门科学，也是一门艺术，如果你理解了所有的研究论文，那么你做得相当不错。对于我们其余的人来说，通过[把你的头缠在神经网络](https://hackaday.com/2017/05/22/wrap-your-mind-around-neural-networks/)上，并尝试[最简单的张量流例子来跟上速度。](https://hackaday.com/2017/03/14/google-machine-learning-made-simpler/)

 [https://www.youtube.com/embed/MjViy6kyiqs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MjViy6kyiqs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

