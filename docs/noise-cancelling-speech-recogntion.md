# 噪声消除语音识别

> 原文：<https://hackaday.com/2016/08/02/noise-cancelling-speech-recogntion/>

如果你和我们一样，你会读得多一点，然后拍拍你的额头。亚马逊最近申请了一项专利。这并不是什么新闻，*本身*——他们申请了很多专利，包括点击按钮订购东西和在白色背景下拍照的专利(以一种非常具体的方式)。然而，[这个专利](http://patft.uspto.gov/netacgi/nph-Parser?Sect1=PTO2&Sect2=HITOFF&p=1&u=%2Fnetahtml%2FPTO%2Fsearch-bool.html&r=43&f=G&l=50&co1=AND&d=PTXT&s1=amazon.AANM.&OS=AANM/amazon)不仅是一个好主意，而且我们感到惊讶的是它不是来自黑客社区。

不可能有一项发明没有问题，而这项发明解决的问题是一个常见的问题:戴着降噪耳机，你听不到你想听到的东西(比如有人在你身后出现)。亚马逊解决方案？让耳机监控可编程的关键词，并根据这些词关闭噪声消除。我们想知道你是否可以有一个更复杂的数字信号处理器来寻找其他线索，如汽车喇叭、警笛或尖叫声。

我们之前已经讨论过修复[商用降噪耳机](https://hackaday.com/2013/12/07/repairing-bose-active-noise-cancelling-headphones/)。如果你不介意走低端技术路线，总会有简单的[方式](https://hackaday.com/2014/05/04/block-noise-listen-to-music/)，但这些方式不太可能适应语音识别。