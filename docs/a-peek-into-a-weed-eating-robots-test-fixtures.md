# 窥视一个吃杂草机器人的测试装置

> 原文：<https://hackaday.com/2018/07/07/a-peek-into-a-weed-eating-robots-test-fixtures/>

说到生产，快就是好！但是第一次*对*更好。任何有助于防止返工的事情都值得投资。一些捕捉问题的最好工具是好的测试夹具。Tertill(去年启动的太阳能除草机器人)的工作人员花时间分享了两个 DIY 测试夹具的简短视频，他们用这些夹具在组装前测试组件。

视频很短，但它们展示了做好测试的所有东西:在[电机测试仪](https://www.youtube.com/watch?v=cWz44rUTbBE)上，没有连接器或电线可以摆弄，测试自动开始，并且通过突出的 led 有清晰的反馈。 [UI 板测试器](https://www.youtube.com/watch?v=uHjY1-j0FQo)也自动启动，并有明确的 LED 反馈，并配备了一个定制的板固定器，其凹槽形状正好适合 PCB。一旦电路板放入，滑板就像抽屉一样被推动，与测试硬件接触，开始测试。两个单元中完美形成的凹槽还起到另一个作用；它们充当被测元件和触点物理形状的通过/不通过测试。

两个视频都嵌在下面；虽然没有太多实际测试硬件的细节，但我们确实发现了一个树莓 Pi 和至少两个 Adafruit 徽标，以及其他黑客熟悉的元素，如激光切割丙烯酸树脂、3D 打印塑料、弹簧针和 PVC 接线盒。

 [https://www.youtube.com/embed/cWz44rUTbBE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/cWz44rUTbBE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/uHjY1-j0FQo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/uHjY1-j0FQo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



你们中的一些人可能还记得大约一年前看到的原型。一年可能很长，但正如阿曼达·沃兹尼亚克所说:一个工作原型意味着事情完成了 15%，有趣的部分结束了。令人欣慰的是， [OpenFixture 项目](https://hackaday.com/2016/10/23/openfixture-takes-the-pain-out-of-pogo-pins/)通过简化弹簧针测试夹具的设计，消除了一些麻烦。