# (LED)墙上的 1575 瓶啤酒

> 原文：<https://hackaday.com/2016/06/03/1575-bottle-of-beer-on-the-led-wall/>

向我的小朋友问好，旧金山 Noisebridge 的成员亲切地给它取名为 [Flaschen Taschen](https://noisebridge.net/wiki/Flaschen_Taschen) 。这证明了他们决心~~喝科罗纳啤酒~~让更多的会员参与每年为湾区创客节建造大型展示。尽管他们的展位非常繁忙，我还是找了几个建筑商进行了采访。当你有一个 9 英尺高，10 英尺宽的巨大的全彩色显示器时，展台挤满了人就不足为奇了。

请观看视频，休息后请和我一起了解他们是如何做到这一点的。

 [https://www.youtube.com/embed/b51vYfy4K2o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/b51vYfy4K2o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



Flaschen Taschen 的灵感来自 C-Base 制造的 [Mate Lite](http://hackaday.com/2014/03/19/massive-led-display-makes-use-of-reused-soda-bottles/) 瓶子展示。最初的展示使用了 Club Mate 瓶——一种在欧洲黑客中流行的能量饮料，它的狂热程度让我们想知道为什么它还没有在更广泛的市场上出现。因此，当 Noisebridge 去建造他们自己的饮料时，他们必须为 1575 个透明玻璃瓶找到不同的捐赠饮料。

[![small-bottles-03](img/ef0c5f7168304a9724631bf9963257a9.png)](https://hackaday.com/wp-content/uploads/2016/06/small-bottles-03.jpg) 他们选定了科罗纳啤酒。但这种选择的一个挑战是，Mate 是用塑料箱包装的，而 Corona 不是。相反，他们从当地市场借来了迪安食品公司的牛奶箱。它们太小了，不适合 5×5 的网格，所以明智的选择是用一些全尺寸 12 盎司的瓶子代替 6.4 盎司的 Coronita 瓶子。这种差异对你的眼睛来说是可以忽略的，而且还有一个额外的好处，就是让瓶子贴合在板条箱里，以获得惊人的像素密度。

成串的 WS2801 发光二极管用于照亮显示器。每箱 25 瓶都有自己的绳子，拴在旁边的箱子上。这使得移动显示器和再次设置显示器变得相当容易管理。一个树莓 Pi 控制一切，达到 160 fps 左右的刷新率。

 [![Rear of the display shows LED strips and foil](img/15ae02cdd9aa63ff34e5af6cbfa7e5cb.png "IMG_1050")](https://hackaday.com/2016/06/03/1575-bottle-of-beer-on-the-led-wall/img_1050/) Rear of the display shows LED strips and foil [![One Raspberry Pi to rule them all](img/5eacf5d63058990888811bb5acf5b259.png "DSC_0259")](https://hackaday.com/2016/06/03/1575-bottle-of-beer-on-the-led-wall/dsc_0259/) One Raspberry Pi to rule them all

点显示器上的漏光是一个很大的问题，这个项目通过几种方式解决了这个问题。每个瓶子都用箔纸可爱地包着(他们用预先切好的食物服务单，就像你的卷饼被包着一样)，以隔离每个像素。带有网格切割的硬纸板可以固定瓶子的颈部。这种隔板的商业面被涂成黑色，以防止光线从显示器后面泄漏，并有助于像素的真正“关闭”状态。

没有显示器是一座孤岛。你可以建造它，但是你需要视觉化的东西来让人群发出呜啊呜啊的声音。Noisebridge 也传达了这一点。他们在众多动画中滚动，比如等离子体和粒子，滚动文本，当然还有玩游戏。Flaschen Taschen 包含了一个由观众玩的 pong 实现。在大 blinkie 和这个经典游戏之间，难怪我们几乎不能进入采访的框架。