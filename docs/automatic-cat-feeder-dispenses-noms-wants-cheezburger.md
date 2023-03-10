# 自动喂猫器分发 Noms，想要芝士汉堡

> 原文：<https://hackaday.com/2015/11/05/automatic-cat-feeder-dispenses-noms-wants-cheezburger/>

[Domiflichi]喜欢他的猫，但不喜欢喂养它们的苦差事。因此，像任何优秀的工程师一样，这个简单的问题成为了他的下一个项目:建造一个自动喂猫器。基于 Arduino，他的发明发出哔哔声，让猫知道该吃饭了，然后把食物分配到几个碗里。还有手动控制的按钮。这让他可以给每只猫单独喂食。DS1307 RTC 跟踪进料时间，完善了特性集。

他的构建中最有趣的部分之一是从试验板到原型板的转换。这通常包括拆开一个工作版本，然后把它重新组装起来，并试图找出它不再工作的原因。[Domiflichi]的问题(在一篇[后续文章](http://jamienerd.blogspot.com/2015/09/automatic-cat-feeder-challenges.html)中详述)是弄清楚如何编程实时时钟模块来设置时间，因为当你断开电源时，它会失去时间。他没有使用 Arduino 对 RTC 进行编程，而是使用了 RTC 芯片的电池备份功能，在他的计算机上进行编程，然后将其焊接到电路板上。芯片就位后，他继续移除备用电池。这种解决方案无疑会让许多读者不以为然地挥舞手指，但它确实有效。

这可能看起来过于复杂，但他的项目值得一试，看看他是如何应对一些工程挑战的。食物漏斗本身是现成的谷物分配器。我们已经看到其他设计[用 3D 打印的螺旋钻](http://hackaday.com/2015/05/31/dual-pet-food-dispenser-is-doubly-convenient/)来引导这种机制。

 [https://www.youtube.com/embed/nS-NIlRqV50?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/nS-NIlRqV50?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

