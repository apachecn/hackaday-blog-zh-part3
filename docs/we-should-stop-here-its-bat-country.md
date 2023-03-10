# 我们应该停在这里，这是蝙蝠国！

> 原文：<https://hackaday.com/2017/08/10/we-should-stop-here-its-bat-country/>

[罗兰·梅尔滕斯]有一个蝙蝠探测器，或者更确切地说，他有一个可以记录超声波的设备——蝙蝠用来回声定位的那种声音。他想要的是蝙蝠探测器。当他发现蝙蝠住在他房子后面时，他开始着手创建一个程序，用他的记录器来探测蝙蝠何时在附近。

[Roland]的工作流程包括将他后院的记录分解成一秒钟的片段，将它们加载到 Python 程序中，并运行一些机器学习代码来确定该片段是否是蝙蝠的记录，并使用它来确定飞来飞去的蝙蝠数量。他使用了几个 Python 库来做这件事，包括 [Tensorflow](https://www.tensorflow.org/) 和 [LibROSA](https://librosa.github.io/librosa/) 。

Python 代码将每个一秒钟的剪辑分成 22 个部分。对于每个部分，他确定样本的最大值、最小值、平均值、标准偏差和最大最小值——如果信号的多个部分具有某些特征(如高标准偏差)，那么软件已经检测到蝙蝠的叫声。有了这个，Roland 开始研究机器学习，这样他就可以卸下探测蝙蝠的工作。他再次求助于 Python 和 Keras 库。

95%的成功率，[罗兰]现在有蝙蝠探测器了！一个也很好用的。有关检测蝙蝠和机器学习的更多信息，请查看超声波项目列表中的[蝙蝠检测器，并查看用于与 Tensorflow](https://hackaday.com/2016/01/16/hacklet-91-ultrasonic-projects/) 和机器学习一起工作的 [IDE。](https://hackaday.com/2017/06/27/machine-learning-ide-in-alpha/)