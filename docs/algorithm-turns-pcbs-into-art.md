# 算法把多氯联苯变成艺术

> 原文：<https://hackaday.com/2016/11/21/algorithm-turns-pcbs-into-art/>

我们中的许多人都曾把电路板举到强光下，以感受它可能包含多少层电路。[alongruss]也这样做了[，但是，不像我们，他看到了艺术](https://hackaday.io/project/18381-pcb-art-medium)

我们之前报道过一些艺术 PCB。这些，在很大程度上，[是关于以某种方式修饰](http://hackaday.com/2013/03/27/turning-pcbs-into-art/)在[的痕迹。](http://hackaday.com/2013/09/24/backlit-pcb-panel-as-wall-art/)它们还产生了工作电路。[alongruss]的作品更关注光线穿过 FR4 的方式:丝网印刷给这幅画增加了一个有趣的维度，以及锡涂层如何反射光线。

为了证明和使用他的算法，他从 GIMP 开始。他让蒙娜丽莎通过一组过滤器，直到他有了可以应用于电路板层的黑白图像层。他从 Seeed Studio 订购了一套电路板，然后等待。

他们成功地回来了！所以他把他的方法编成了处理代码。如果你想玩玩，可以看看他的 [GitHub](https://github.com/alongruss/PCBArt_Eagle) 。