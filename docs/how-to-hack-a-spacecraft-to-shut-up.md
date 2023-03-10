# 如何黑掉一艘飞船优雅地死去

> 原文：<https://hackaday.com/2016/10/03/how-to-hack-a-spacecraft-to-shut-up/>

上周，罗塞塔飞船在 2014 年绕彗星 67P/Churyumov-Gerasimenko 运行后撞上了它。它应该这样做:任务结束了，任务设计者想通过近距离观察彗星表面来结束它。但这提出了一个有趣的问题:[你如何让一个被设计成永不停止的设备实际上停止](http://blogs.esa.int/rosetta/2016/09/29/how-rosetta-gets-passivated/)？


像 Rosetta 这样的航天器是从头开始建造的，以保持运行，重新启动并进入备份模式，如果遇到问题，给家里打电话并等待指示。这叫安全模式，在之前已经[救过飞船好几次了。如果它不被固定，当航天器撞上彗星时，它会触发一种特殊的安全模式，称为 FDIR(故障检测，隔离和恢复)，它会不断向地球发送诊断信号，直到任务控制器做出反应。](http://blogs.esa.int/rosetta/2016/05/30/rosetta-safe-mode-5-km-from-comet/)

但这项任务已经结束，如果探测器不断重启并发送求救信号，它可能会干扰使用相同频率的其他航天器。即使是微弱的信号也可能干扰另一艘飞船，所以设计者想彻底关闭它。因此，他们使用了一种有趣的方法:他们在飞船上安装了软件来阻止它给家里打电话。在它撞上彗星的前一天，他们给它发送了一个补丁，取消了安全模式，取而代之的是自发射前就没有使用过的被动模式，如果遇到问题，航天器只会坐着等待指示。坠毁前几个小时，这个补丁被激活，探测器现在没有备用计划。因此，当它撞上彗星时，它进入了被动模式，只要电池耗尽，它就会保持这种模式，永远等待一个永远不会到来的重新启动命令…

感谢[丹尼尔]的提示！

 [https://www.youtube.com/embed/lVKFyFbfpOI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lVKFyFbfpOI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

