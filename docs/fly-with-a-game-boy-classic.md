# 与 Game Boy 经典一起飞

> 原文：<https://hackaday.com/2016/08/21/fly-with-a-game-boy-classic/>

有多少成年的硬件黑客在他们的游戏机上玩俄罗斯方块或马里奥来消磨他们的青春？对许多人来说是美好的回忆，但除非你很幸运，否则你的游戏机可能会消失很久。不过，对[戈蒂埃·哈滕贝格]来说，他在父母家有了一个意外的发现；他的 Game Boy 经典，那些年无人问津，被人遗忘。对我们来说幸运的是，他的第一个想法是他是否可以用它作为无人机的控制器，更好的是[他分享了他的工作给我们所有人看](https://blog.paparazziuav.org/2016/08/01/drones-vs-retro-gaming-fly-with-a-game-boy-classic/)。

[![How to connect a drone and a Game Boy](img/775bd8133db5a4d8c150dcb70d81c930.png)](https://hackaday.com/wp-content/uploads/2016/08/wiring.jpg)

How to connect a drone and a Game Boy

过去，一个潜在的游戏机黑客可能会被任天堂针对游戏盗版的法律辩护所阻止，但受益于几十年的发展，掌上游戏机的硬件现在是一目了然的。对戈蒂埃来说不幸的是，他似乎是第一个使用无人机作为飞行控制器的人，所以他不得不自食其力。他的 Game Boy Game Link 串口馈入 Arduino/FTDI 组合，将游戏链接转换为 USB，然后发送到他的笔记本电脑上，一个小软件通过[狗仔队无人机框架](http://wiki.paparazziuav.org/wiki/Main_Page)将它们转换为无人机的命令。

他所有的代码都在 GitHub 库里[，他上传了一段他的工作视频，你可以在视频下方看到。对于一个 90 年代初的孩子来说，仅仅是想到他们的掌上游戏机可以做到这一点就已经令人兴奋不已了！](https://github.com/enacuavlab/PPRZonGB)

 [https://www.youtube.com/embed/LoLxrchwSpo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LoLxrchwSpo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



也许不出所料，我们多年来报道的大多数任天堂游戏机黑客都有游戏味道，所以这是第一款游戏机飞行控制器。大约在 1991 年，我们迫切需要的黑客产品是 Game Boy 示波器盒，虽然这似乎是另一个尚未被征服的产品，但我们已经推出了相反的产品:作为 Game Boy 显示器的[示波器](http://hackaday.com/2011/02/14/nintendoscope/)。

谢谢[Piotr]的提示。