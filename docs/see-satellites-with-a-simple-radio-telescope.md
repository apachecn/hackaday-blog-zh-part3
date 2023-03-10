# 用简单的射电望远镜看卫星

> 原文：<https://hackaday.com/2017/03/23/see-satellites-with-a-simple-radio-telescope/>

你有备用的碟形网络天线吗？它们并不太难得到，无论是在垃圾日的路边，还是在自由循环日。如果你能找到一个，你可能想试试这个有趣的射电望远镜。

现在，不要对[Justin]的简约风格有太多期待。毕竟，你将从一个相当小的天线和 Ku 波段的 LNB 开始，所以你不会做严肃的射电天文学。事实上，BOM 并不包括一个花哨的接收器——只是一个被黑客入侵的卫星探测器。这个想法是仅仅获得一个射电源的相对“亮度”读数，而不需要尝试解调信号。为此，驱动 sat finder 中压电蜂鸣器的信号通过前置放大器输入 Arduino。Arduino 还控制步进电机来控制碟形天线的方位角和仰角，这让它可以扫描天空并建立信号强度的地图。结果是一条清晰的亮点带，代表着从[贾斯汀]在巴西的位置可以看到的地球同步卫星。

修改肯定在[贾斯汀]的日程表上，包括更好的设备，这将使他能够对银河中心成像。在我们对基于 SDR 的小型射电望远镜的报道中，或者从 T2 这个可以收听木星的定制接收器中，可能会给他一些提示。

 [https://www.youtube.com/embed/aeah3fFYlnA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/aeah3fFYlnA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

