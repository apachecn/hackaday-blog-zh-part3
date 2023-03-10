# 电脑学会黑国际象棋

> 原文：<https://hackaday.com/2015/10/02/computer-learns-to-hack-chess/>

很多电脑会下棋。长颈鹿是一台国际象棋计算机，但与其他常见的国际象棋程序不同，长颈鹿是自学的。它显然也学得很好，因为它在 FIDE 等级上被评为国际大师(在 2.2%的玩家中名列前茅)。顶级的国际象棋计算机达到了超级大师的水平，但它们不是自学成才的。

[马修]把这项工作作为他硕士学位项目的一部分。他的论文涵盖了长颈鹿的算法如何不同于使用神经网络方法的传统国际象棋程序(见下面的视频中的一些技术)。[马修的]神经网络不是对不同棋盘位置的相对优势进行编码，而是从真实的棋盘位置(从棋步数据库修改而来)开始训练，并参与游戏的双方。经过多次迭代，C++神经网络发展出自己的一套规则。这需要检查每个位置的 350 多个特征(例如，是否允许阉割，或者滑动件可以移动多远)。

虽然国际象棋游戏可能是一个利基项目，但可以推导复杂评估函数的神经网络在计算机视觉、股票市场预测和优化等领域具有广泛的适用性。当然，我们想把长颈鹿和下棋机器人联系起来。无意冒犯之前的帖子，但我们想象长颈鹿会和下棋的[一起拖地板。](http://hackaday.com/2013/09/15/tiny-chess-playing-computer/)

 [https://www.youtube.com/embed/STjW3eH0Cik?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/STjW3eH0Cik?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

