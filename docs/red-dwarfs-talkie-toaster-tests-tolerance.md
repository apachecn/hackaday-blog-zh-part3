# 红矮星的有声烤面包机测试耐受性

> 原文：<https://hackaday.com/2016/11/21/red-dwarfs-talkie-toaster-tests-tolerance/>

在红矮星电视剧中，有声烤面包机想知道你是否想要烤面包，如果不是烤面包，那么也许是松饼或华夫饼，它会不停地纠缠你，直到你用 14 磅的锤子砸碎它，并扔进废物处理器。现在[slider2732]实际上已经走了，[制造了一个地狱机器](https://www.youtube.com/watch?v=QUQrripCRuM)！

他在烤面包机手柄中隐藏了一个 PIR 传感器，当有人不幸路过时，它会告诉 Arduino Pro Mini。Arduino 然后从 SD 读卡器中读取声音文件，并通过一个 3 瓦的放大器播放给扬声器。为此，他使用了 github 上的 TMRpcm 库。

[slider2732]巧妙地将扬声器安装在烤面包机的侧面，并配有一些形状合适的零件和一些 led，使其看起来和工作起来很像真正有声烤面包机上发光的圆形面板。我们鼓励你在休息后观看视频，除非你真的想吃烤面包。作为一个安慰，视频也走过制作过程。

 [https://www.youtube.com/embed/QUQrripCRuM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/QUQrripCRuM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



这些链接会带你去看电视剧《有声电影烤面包机》中的片段:被砸之前的片段[和被修理之后的片段](https://www.youtube.com/watch?v=7folKbch3U8)和[。](https://www.youtube.com/watch?v=LRq_SAuQDec)

你还能用烤面包机做什么？为什么不[做一个会飞的](http://hackaday.com/2013/11/13/flying-rc-toaster/)。当然，在 Hackaday 上最受欢迎的似乎是用烤面包机制作回流焊炉的[。](http://hackaday.com/2013/11/21/a-pair-of-toaster-reflow-oven-builds/)