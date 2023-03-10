# Mathieu Stephan:安全开源硬件密码管理器的制作

> 原文：<https://hackaday.com/2017/11/30/mathieu-stephan-the-making-of-a-secure-open-source-hardware-password-keeper/>

Mathieu Stephan 是一名开源硬件开发人员，一名总是有库存的 Tindie 卖家，一名前 Hackaday 作家，一个令人敬畏的全能家伙。过去几年他最大的项目之一是 Mooltipass，这是一个基于智能卡和 USB 接口的离线密码管理器。这是解决贴在你的显示器上的便利贴的方法，而且你在互联网上的所有账户都使用同一个密码。

Mooltipass 是一款非常成功的产品，去年 Mathieu 推出了 Mooltipass Mini。不，它没有可爱的发光触摸感应按钮，但它比它的老大哥便宜一点，对物理攻击的抵抗力更强一点——这是你希望在一个保护你所有密码安全的设备中看到的。

然而，马蒂厄并不是唯一一个建造 Mooltipass 的人。这是一个开源项目，有来自世界各地的开发人员和测试人员。它可能是从一个黑客帖子开始的，但是现在 Mooltipass 已经成长为一个全球性的开发团队，其贡献者遍布全球。马修是怎么做到的？你可以在下面的 2017 年 Hackaday 超级大会上查看他的演讲。

 [https://www.youtube.com/embed/McUGIoElYnY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/McUGIoElYnY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



那么，你如何与分布在从加利福尼亚到瑞士到新西兰的数十个开发者合作呢？Mathieu 找到的最佳解决方案是通过共识实现特性，显然是使用 GitHub 进行版本控制和源代码控制，并实际记录代码。这些都是显而易见的解决方案，但是最佳实践并不完全是常见的实践。

交流是在群体中进行的，而不是通过即时消息、电子邮件或某种信息服务这样的直接联系。几乎所有的事情都是通过谷歌小组和一个 Trello board 完成的，这是一个方便的工具，可以把任务放在日历上。这是一个为 Mooltipass 团队工作的系统，与许多开源项目不同，新手很容易理解实际发生的事情。

但这是一个硬件项目，而且是一个安全的硬件项目。这意味着 Mooltipass 需要防篡改且难以进入。第一个 Mooltipass 有一个塑料版本，但对于 Mooltipass Mini，该团队采用了全铝。这需要 CNC，对于 Mooltipass Mini 来说，这意味着中国的机加工车间。Mathieu 实际上是去了中国制造这些多用途通行证，并发现了中国制造业的一些令人惊讶的方面。铣削外壳最便宜的供应商实际上是最可靠的。显然，你永远不知道你会得到什么。组装是一个问题，不仅仅是因为语言障碍。然而，马修发现了一个有趣的解决组装问题的方法:制作一个视频。这是如此简单，如此明显，但哦，如此聪明。

Mooltipass 和 Mooltipass mini 是开放硬件的绝佳范例。但是接下来呢？下一代 Mooltipass 正在研发中，有望更加安全。这款下一代 Mooltipass mini 将拥有蓝牙和一个禁用它的硬件选项，相同的智能卡接口和一个安全的微控制器。这有望成为保存密码的最佳方式，我们已经迫不及待地想看看 Mooltipass 团队的实验室成果。