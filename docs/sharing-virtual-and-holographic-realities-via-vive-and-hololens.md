# 通过 Vive 和 Hololens 分享虚拟和全息现实

> 原文：<https://hackaday.com/2017/02/02/sharing-virtual-and-holographic-realities-via-vive-and-hololens/>

[Drew Gottlieb]的一个混合现实和虚拟现实的实验性[项目](http://drewgottlieb.net/2017/01/31/mixing-reality-with-vr.html)使用微软 Hololens 和 HTC Vive 展示了两个用户成功共享一个工作空间和控制器。当 VR 用户用一个简单的应用程序在半空中绘制立方体时，Hololens 用户可以看到相同的立方体被创建并映射到现实世界的位置，两个耳机甚至可以在同一个共享空间中进行交互。你真的需要看看下面的视频，才能完全理解这有多酷。

两个或更多的 VR 或 AR 用户共享同一个虚拟环境并不新鲜，但以两个非常不同的耳机共享的方式将虚拟环境锚定到现实世界中是很有趣的。[Drew]说，真正的挑战不仅仅是让不同的硬件相互对话，而是如何让它们对共同的空间有共同的理解。[Drew]需要一种方法来实现这一点，您可以在下面嵌入的视频中看到结果。

由于只有几天时间来进行概念验证，[Drew]采用了一种快速而肮脏的解决方案。为了对齐虚拟和真实的房间空间，Hololens 用户首先拿起一个 Vive 控制器，并被提示手动将其与浮动虚拟控制器对齐。一旦用户手动对齐这些虚拟和现实世界的点，软件就使用该交叉点作为锚，将现实和虚拟对象锁定在对空间的相同理解中。这甚至比预期的更好，但是有一些微小的误差，因为手动校准从来不是完美的。偏离一度在对准点附近不会有太大的影响，但是当你远离时，不对准就会增加。[Drew]指出，促进三个点而不是一个点的对齐将是通向更好结果的一步。

共享环境由一个简单的积木式应用程序组成，由 Vive 控制器操纵，但独立于实际的耳机。因此，您不需要实际使用 VR 头戴设备。你可以将 Hololens 与 VR 控制器配合使用，并在房间中央创建一些立方体，而不是在空的虚拟空间中。此外，其他人可以戴上 VR 头戴设备(或另一个 Hololens)，不仅可以看到，还可以在相同的环境中进行交互。

如果你有 Vive 和 Hololens，并且想自己尝试一下，[Drew]在 GitHub 上有所有代码[。](https://github.com/dag10/HoloViveObserver)

 [https://www.youtube.com/embed/XPYb2IsZL68?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XPYb2IsZL68?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



混合现实作为一个领域正在复苏，并充满了有趣的发展。我们最近[发表了一篇文章](http://hackaday.com/2017/01/09/david-krum-the-revolution-in-virtual-reality/)，讲述了 AR 和 VR 中的事物是如何发展的。有兴趣在这一领域做出自己的创新吗？即将推出的用于 Vive 的[追踪硬件](http://hackaday.com/2017/01/22/vive-tracker-brings-easier-vr-hacking/)显然是为了让新想法的开发更容易。