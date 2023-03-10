# 点燃 750 个树莓馅饼

> 原文：<https://hackaday.com/2018/01/24/firing-up-750-raspberry-pis/>

创建 Raspberry Pi 集群是一种流行的黑客活动。Bitscope 已经将这些集群商业化一段时间了，去年他们为洛斯阿拉莫斯国家实验室创建了一个由 750 个 Pis 组成的集群。你可能想知道一个以超级计算机闻名的机构想要一堆树莓派。事实证明，仅仅为了测试软件而关闭一个真正的高速集群是不合理的。现在，开发人员可以用大量的 CPU 内核运行小型测试程序，而不需要花费时间。

从表面上看，这听起来并不太难，但连接 750 个任何东西都有其挑战性。你必须提供能量并带走热量。它们都必须进行通信，你不会想把这个东西放在几百平方英尺的地方，这样会使加热和供电更加困难。

[系统是模块化的](http://cluster.bitscope.com/)，每个模块包含 144 个活动节点、6 个备用节点和一个集群管理器。这一切都适合 6U 机架外壳。Bitscope 指出，您可以在 42U 中部署 1000 个节点，包括网络结构和冷却在内的功耗约为 6 千瓦。这听起来很多，但对于 1000 个节点的设备来说，这非常经济。成本也不低，1000 个节点的运行成本约为 15 万美元。当然，这也是很多，但不能和其他选择相比。

在之前，我们已经见过[相当大的π星团。如果你真的想去小和低功耗，你总是可以尝试](https://hackaday.com/2014/10/07/120-node-rasperry-pi-cluster-for-website-testing/)[集群圆周率零](https://hackaday.com/2017/10/11/terrible-cluster-of-pis/)。