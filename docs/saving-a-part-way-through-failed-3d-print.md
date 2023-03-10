# 保存中途失败的 3D 打印

> 原文：<https://hackaday.com/2017/06/03/saving-a-part-way-through-failed-3d-print/>

这将是所有 3D 打印机所有者的共同体验；一个长打印大部分做好了，出了点问题。结果:大部分指纹和一堆塑料粉丝，或者更糟的是，一个带有明显偏移层的指纹。

[Simon Merrett]在他的打印机上运行了很大一部分，在 2.5 小时到 3 小时的打印中，喷嘴抓住了他已经完成的内容的边缘，结果他被挤压到稀薄的空气中(他在他的提示电子邮件中告诉我们，他的机器制造可能是罪魁祸首)。幸运的是，他看到了这一切的发生，他能够按下他的 Repetier 软件中的停止按钮，让灾难迅速停止。

他如何挽救这种情况是一个有趣的故事，他在我们放在断点下方的截屏视频中记录了这个故事，它涉及到使用电子表格来分析 g 代码，并删除他已经打印的部分的线条，然后插入一组新的 Z 轴尺寸，从床身向上开始打印的剩余部分。再做一些修改，他就可以打印出他的部分的剩余部分，然后他可以把它粘在已经打印好的部分的未完成部分的顶部。他在他的 YouTube 描述中指出，他给 Repetier 的人发了电子邮件，他们告诉他一种更快的方法来处理 Z 轴:使用 G92 命令来重置它。

你可能会问，如果他准备花这么多时间，他为什么不干脆重印整个部分。但他指出，在这种情况下，印刷很可能会在同一点上再次失败。

 [https://www.youtube.com/embed/BFSNYqddBEA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/BFSNYqddBEA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



如果你不能拿起一个失败的印刷品来完成它，那么[回收你失败的印刷品](http://hackaday.com/2016/11/08/fail-of-the-week-upcycling-failed-3d-prints/)怎么样？