# 使用神经网络解码 Enigma

> 原文：<https://hackaday.com/2017/08/11/decoding-enigma-using-a-neural-network/>

[Sam Greydanus]创造了一个神经网络[，它可以像 Enigma 一样编码和解码信息](https://greydanus.github.io/2017/01/07/enigma-rnn/)。对于那些不知道的人来说，[英格玛机](https://en.wikipedia.org/wiki/Enigma_machine)是二战期间德国人用来加密和解密信息的最著名的机器。给神经网络一些加密文本，称为密文，以及用于加密文本的三个字母的密钥，网络预测原始文本或明文的准确率约为 96-97%。

他使用的神经网络类型是长短期记忆(LSTM)网络，这是一种循环神经网络(RNN)，我们在我们的[文章中谈到过，该文章涵盖了多年来开发的许多不同类型的神经网络](http://hackaday.com/2017/06/08/from-50s-perceptrons-to-the-freaky-stuff-were-doing-today/)。rnn 是[图灵完全的](https://en.wikipedia.org/wiki/Turing_completeness)，这意味着它们可以逼近任何函数。[Sam]注意到了其中的讽刺意味，即艾伦·图灵不仅提出了图灵完备性的概念，而且在破解二战中使用的谜团中发挥了重要作用。

[山姆]是怎么做到的？

对于这种应用，RNNs 和 LSTMs 的一个关键是它们善于从序列形式的数据中学习，在这种情况下是字母字符的序列。当对整个文本文档进行训练时，他们学习单词、标点符号和句子结构。在 Enigma 的例子中，[Sam]用随机生成的明文、随机生成的密钥和使用 [crypto-enigma Python API](https://crypto-enigma.readthedocs.io/en/latest/machine.html) 生成的密文来训练他的 LSTM。从那次训练中，LSTM 网络了解了英格玛的配电盘、轮子和电缆的大致情况。请注意，虽然它可以处理不同的钥匙，这意味着它可以处理转向不同位置的车轮，但它只使用一种电缆配置和内置于车轮中的电线对加密的数据进行了训练。你可以在【山姆】的 [GitHub 页面](https://github.com/greydanus/crypto-rnn/tree/master/enigma-rnn)上找到神经网络的完整代码。正如你可以从这篇文章的标题中看到的，它在进行预测(即解码)时有 96-97%的准确率。

在第二次世界大战结束时，大多数英格玛机器都被摧毁了，但我们的[布莱恩·本考夫]很幸运地在东部参加一个老式计算机节时看到了一些损坏和修复的机器。但是当然，谁能抗拒制造一个，一个例子是[这个有 3D 打印部件的](http://hackaday.com/2016/10/21/3d-print-an-enigma-machine-thats-close-to-the-real-thing/)。这里还有更多[等着你去看。](http://hackaday.com/tag/enigma-machine/)