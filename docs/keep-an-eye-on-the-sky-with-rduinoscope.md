# 用望远镜观察天空

> 原文：<https://hackaday.com/2017/04/11/keep-an-eye-on-the-sky-with-rduinoscope/>

我们都喜欢仰望晴朗的夜空，惊叹于星空的壮丽。我们中的一些人甚至将望远镜对准特定的天体以获得更近的视野。任何曾经观察过木星以外任何东西的人都知道其中的麻烦。最不幸的是，我们居住的星球恰好绕着一个固定的轴旋转，这使得在你的视野中保持一个天体有些困难。

将几个步进器和一些硅脑绑在一个观测仪器上来对抗地球的自转并不需要太多，这样的系统已经存在了几十年。不幸的是，它们非常昂贵。所以[Dessislav Gouzgounov]自己动手开发了[rDuinoScope——一个开源望远镜控制系统](http://rduinoscope.co.nf/index.html)。

基于 Arduino Due，该系统存储了 250 个恒星物体的数据库。结合 RTC 和 GPS，rDunioScope 可以定位并锁定你最喜欢的星云并跟踪它，让你平静地观看它。请务必[获取代码](https://github.com/dEskoG/rDUINOScope)并在您设置好自己的 rDuinoScope 后告诉我们！