# 婴儿用蓝牙音箱

> 原文：<https://hackaday.com/2017/12/11/a-bluetooth-speaker-for-babies/>

[Modustrial Maker]的[Mike Clifford]有不止一个，不是两个，而是五个朋友打电话给他，告诉他他们的第一个孩子就要出生了，他受到启发，为他们制作了一个带有独特 LED 矩阵显示屏的蓝牙音箱作为合适的礼物。不仅是为了娱乐客人，也是为了从视听上刺激他们的每个孩子，促进他们的神经发育。

[Clifford]拿起粗糙的枫木板并刨平，在涂上木材饰面之前，建造了一个斜接的盒子来容纳组件。盒子里的大脑是一个 Arduino Mega——或者一个合适的克隆——控制一个 Dayton 蓝牙音频和 2x15W 放大器板。除了 19.7V 电源外，Mega 还有一个降压转换器，以及一个麦克风，使 LED 矩阵具有声音反应能力。LED 矩阵位于可移动挡板上，以调节它和半透明丙烯酸光漫射器之间的距离。这可以在尖锐点或更柔和的混合外观之间转换光线，非常适合滚动矩阵文本和壁炉效果！看看吧！

 [https://www.youtube.com/embed/X1bEgGLwVLY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/X1bEgGLwVLY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[Clifford]的 Arduino 代码在 [GitHub](https://github.com/modustrialmaker/Audio-Reactive-LED-Matrix) 上发布，供任何有朋友怀孕的人使用。你永远不知道你小时候的[费雪牌卡带播放器](https://hackaday.com/2015/08/07/fisher-price-bluetooth-speaker-hack/)什么时候会派上用场。