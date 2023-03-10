# 33C3:你怎么能相信你的随机数呢？

> 原文：<https://hackaday.com/2017/02/01/33c3-how-can-you-trust-your-random-numbers/>

在第 33 届混沌通信大会上，一个突出的话题是关于伪随机数发生器的。[Vladimir Klebanov](右)和[Felix drre](左)提供了一个框架，以确保 PRNGs 做他们应该做的事情。在这个过程中，他们发现了 Libgcrypt/GNUPG 的一个缺陷，并修复了这个缺陷。Woot。

[![mpv-shot0012-zoom](img/35bef1ede1402ebdb1e93d38f65beed1.png)](https://hackaday.com/wp-content/uploads/2017/01/mpv-shot0012.jpg) 密码安全随机数其实事关重大，很多。如果你够老了，还记得 2008 年 Debian OpenSSL 的崩溃，基本上每一个互联网服务都因为糟糕的随机数而存在后门。所以它们很重要。[Vladimir]证明了编写好的随机数生成器是非常非常困难的。因此，非常非常好地测试他们的输出是非常重要的。

那么我们如何测试它们呢？[Vladimir]对我们的第一直觉发出警告，运行像[die hard](https://en.wikipedia.org/wiki/Diehard_tests)这样的统计测试套件。他(正确地)指出，通过足够好的哈希函数运行任何算法都会通过统计测试，但这并不意味着它对密码学有好处。


相反，有两种方法可以测试 PRNG。首先，如果您正在使用一个标准函数，并且有一组参考种子和输出，请检查它们。至少您将验证您的代码正在做它应该做的事情。其次，更普遍的是，你要确保算法不会丢失熵——[prng 不会产生随机性](http://hackaday.com/2015/12/28/v8-javascript-fixes-horrible-random-number-generator/)，所以它们能做的最好的事情就是不丢失熵。

这里有一些你可以检查的东西。如果种子的一部分不影响输出，或者如果两个种子产生相同的输出，或者等价地，如果可能的输出比种子少，那么算法就失去了熵。如果您可以运行任意数量的种子和输出，您可能会蛮力这个测试(希望在宇宙不可避免的热死之前)。

或者你可以分析一下。他们使用 [CBMC](http://www.cprover.org/) 和 [Minisat](http://minisat.se/) 静态分析工具测试了六个 PRNG 实现，以测试这些需求。这样做抓住了所有他们预料到的问题，以及一个他们没有预料到的问题。使用他们的“熵镜”,他们通过程序流程追踪熵的损失，找到错误，并扭转局面。

这不是一个关于密码编程的初学者讲座，但它是一个非常好的讲座。看起来随机的 PRNGs，通过了统计测试，仍然会丢失熵。正如两人在问答中指出的，在合理的时间内确定的唯一方法是仔细阅读代码并验证它不是。这意味着唯一安全的 PRNG 是一个开源的 PRNG。但你已经知道了，对吗？

[https://media.ccc.de/v/33c3-8099-how_do_we_know_our_prngs_work_properly/oembed](https://media.ccc.de/v/33c3-8099-how_do_we_know_our_prngs_work_properly/oembed)