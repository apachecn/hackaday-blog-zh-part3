# 带内信令:昆达音

> 原文：<https://hackaday.com/2017/09/19/in-band-signaling-quindar-tones/>

到目前为止，在这个关于带内信令的简短系列中，我们研究了提供控制信号和传输主要内容的两种常用方法:[用于按键拨号的 DTMF】和用于双向无线电的](https://hackaday.com/2017/09/05/in-band-signaling-dual-tone-multifrequency-dialing/)[编码静噪系统](https://hackaday.com/2017/09/13/in-band-signaling-coded-squelch-systems/)。在这一期中，我们将看看一些很少有人用过，但几乎每个人都听说过的东西:昆达音。

### 什么是昆达？

你可能从未听说过昆达音是什么，但如果你看过任何载人航天视频，你肯定听过它们。昆达音是当美国宇航局与宇航员通信时听到的短哔哔声，正如阿波罗 11 号期间在休斯顿和澳大利亚金银花地面站之间进行的无线电网络检查中听到的那样:

 [https://www.youtube.com/embed/AYyXQcuo8wA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/AYyXQcuo8wA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



如果你仔细听控制器的五次计数，你会听到两个略有不同的音调。较高音调(2525 赫兹)出现在声音传输之前，而较低音调(2475 赫兹)出现在声音传输之后。这些标志性的 250 毫秒哔哔声被称为昆达音。

那么他们做了什么？如果你认为它们是某种“罗杰哔哔声”,用来自动发出信号，表明频道畅通，可以转向另一方通话，这是可以理解的。这是可以理解的，因为今天许多双向无线电，甚至是廉价的家庭无线电服务对讲机，都有某种罗杰哔哔声。就我而言，我一直认为这些哔哔声类似于覆盖在被记录的电话对话上的声音，就像你拨打 911 一样。不过，如果我稍微想一想，我就会意识到，宇航员们会痛苦地意识到，他们所说的一切都被记录下来，留给后代，不需要任何提醒。

### 真正的远程控制

当你考虑载人航天任务的规模时，昆达·托尼斯有一个更实际的目的。在收音机上键入麦克风通常会关闭将麦克风切换到音频电路的触点，并使给发射机供电的继电器跳闸，从而允许操作员在广播中讲话。当收音机放在你面前的桌子上时，或者甚至当它在走廊尽头时，这种方式都很好。但是远程发射器存在一个问题，因为操作员位置和收发器之间的电缆变得难以管理。

在美国宇航局的情况下，休斯顿的任务控制中心不得不使用全球地面站网络，与轨道上或前往月球的任务保持持续联系。像用于星际任务通信的[深空网络](http://hackaday.com/2017/07/21/serious-dx-the-deep-space-network/)一样，美国宇航局需要多个站点来确保当地球旋转时，至少有一个天线可以看到航天器。昆达音以系统制造商[昆达电子](http://www.qeiinc.com/History.aspx)命名，是一种带内信号形式，允许美国宇航局使用同一组租赁线路向收发器发送音频，并在接收和发送之间切换。高音打开发射机，低音关闭发射机。

### 但并不总是如此

昆达音只用于控制美国国家航空航天局的地面站，所以没有必要让飞船无线电使用它们。事实上，美国宇航局采取措施阻止宇航员听到这些声音。太空舱的通讯是全双工的，这意味着宇宙飞船有可能转发它接收到的任何昆达音，这可能会干扰地面站的控制。因此，在上行音频中插入了陷波滤波器，以滤除两种音调；频率如此接近，一个滤波器就足够了。然而，它并不完美，你仍然可以在阿波罗 13 号的这个标志性片段中听到剩余的结尾音调:

 [https://www.youtube.com/embed/y30VxhWQdsM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=69&wmode=transparent](https://www.youtube.com/embed/y30VxhWQdsM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=69&wmode=transparent)



可立即识别的昆达音被用于所有双子座和阿波罗任务的带内信号，甚至在航天飞机时代也派上了用场。现在他们甚至激发了一些有趣的电子音乐。