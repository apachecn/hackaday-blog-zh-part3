# 会说话的神经网络

> 原文：<https://hackaday.com/2016/12/03/talking-neural-nets/>

语音合成并不是什么新鲜事，但它最近变得更好了。多亏了 DeepMind 的 WaveNet 项目，它还会变得更好。字母表(或者是谷歌？)项目使用神经网络来分析音频数据，它通过例子来学习说话。与其他文本到语音转换系统不同，WaveNet 一次创建一个声音样本，并提供令人惊讶的人类声音结果。

在你急于评论“不是黑客！”你应该知道我们正在 GitHub 上看到使用该技术的项目。比如有【ibab】的[具体实现](https://github.com/ibab/tensorflow-wavenet)。[汤姆·派恩]有[一个优化版本](https://github.com/tomlepaine/fast-wavenet)。除了学习英语，他们还成功地将它训练成了普通话，甚至是音乐。如果你不想自己建立一个系统，原始文件有音频文件(大约在中间)，比较传统的参数和拼接语音与 WaveNet 语音。

另一个有趣的项目是反向路径——教 [WaveNet 将语音转换成文本](https://github.com/buriburisuri/speech-to-text-wavenet)。不过，在你变得太兴奋之前，你可能想记下《自述文件》中的这段话:

> “我们已经在单个 Titan X GPU 上训练了该模型 30 个小时，直到 20 个历元，该模型在 13.4 ctc 丢失时停止。如果你没有 Titan X GPU，把 train.py 文件中的 batch_size 从 16 减少到 4。”

据我们所知，你可以用不到 2000 美元买到一台 Titan X。

有一个关于强化学习的多部分讲座系列(DeepMind 的基础)。如果你想自己解决一个项目，这可能是一个很好的起点(第一部分出现在下面)。

我们之前看过 DeepMind [下围棋](https://hackaday.com/2016/03/09/ask-hackaday-google-beat-go-bellwether-or-hype/)。然而，我们不得不承认，比起玩石头，我们得到了语音分析实用的一面。我们正等着报道第一个使用这项技术的黑客项目。

 [https://www.youtube.com/embed/2pWv7GOvuf0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2pWv7GOvuf0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

