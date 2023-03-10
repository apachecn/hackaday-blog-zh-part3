# 用网络摄像头数鸡蛋

> 原文：<https://hackaday.com/2016/10/14/counting-eggs-with-a-webcam/>

为了这一点，你必须翻出你的法语词典(或者[谷歌翻译](https://translate.google.com/translate?sl=auto&tl=en&js=y&prev=_t&hl=en&ie=UTF-8&u=https://fr.eggs-iting.com/blog/prototypage/detection-des-oeufs-dans-un-nid-de-poule.html&edit-text=&act=url)),但这是值得的。【尼古拉斯·吉劳德】一直在[试验用网络摄像头检测鸡舍里鸡下了多少蛋的方法。这个页面记录了这些实验，这些实验使用许多不同的算法来自动检测蛋的数量并通知主人。这个系统很简单，围绕一个运行](https://fr.eggs-iting.com/blog/prototypage/detection-des-oeufs-dans-un-nid-de-poule.html) [Debian Jesse Lite](https://www.raspberrypi.org/forums/viewtopic.php?t=127060) 的 Pi 和一个便宜的 USB 摄像头构建。一个 GPIO 引脚上的 LED 照亮鸡蛋，然后相机捕捉图像进行分析。

【Nicolas】尝试检测颜色和[斑点检测](https://en.wikipedia.org/wiki/Blob_detection)(微生物学家用来计数载玻片上的细胞)，但它们在吸管的不均匀背景下效果不佳。最后，他决定使用一种叫做[局部二进制模式](http://www.pyimagesearch.com/2015/12/07/local-binary-patterns-with-python-opencv/)的技术，其中系统查看一个区域及其周围区域的关系，搜索由鸡蛋的圆形和颜色梯度创建的特定模式。经过一些调整，他声称 100%的成功率。

他的工作是一个名为[产蛋](https://fr.eggs-iting.com/)的项目的一部分，该项目是设计一个易于使用的鸡舍，任何人都可以在他们的后院建造和使用。我养了鸡，在雨雪中漫步去捡鸡蛋，却发现母鸡没有心情，还没有下蛋。因此，一个简单的系统，让我知道有多少鸡蛋期待听起来很完美。