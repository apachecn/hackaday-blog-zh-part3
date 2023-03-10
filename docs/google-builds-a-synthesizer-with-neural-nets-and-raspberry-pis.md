# 谷歌用神经网络和树莓 pi 构建了一个合成器。

> 原文：<https://hackaday.com/2018/03/16/google-builds-a-synthesizer-with-neural-nets-and-raspberry-pis/>

人工智能是新的热点！又到了 1965 年或者 1985 年！我们在人工智能 Rennisance Mk. 2 中，谷歌试图展示人工智能如何让创作者更具创造力[发布了一个围绕神经网络](https://nsynthsuper.withgoogle.com/)构建的合成器。

NSynth Super 是 Magenta 的一个实验性物理接口，Magenta 是大 G 内部的一个研究小组，旨在探索机器学习工具如何以新的方式创造艺术和音乐。NSynth Super 通过将一个 Kaoss 面板、听起来像一般 MIDI 补丁的样本和一个神经网络混合在一起来实现这一点。[![](img/b38da40334e9f72c360fcb9593de27af.png)](https://hackaday.com/wp-content/uploads/2018/03/neural.png)

NSynth 是这样工作的:NSynth 硬件接受来自键盘、DAW 或其他设备的 MIDI 信号。这些 MIDI 命令被输入到一个 openFrameworks 应用程序中，该应用程序使用预编译的(带有 Machine Learning！)各种仪器的样品。这个 openFrameworks 应用程序根据用户通过 NSynth 控制器输入的任何内容来组合和混合这些样本。如果你曾经想听听小鼓和巴松管的组合是什么样的，这就可以了。基本上，你看到的是一个控制 rompler 的 Kaoss pad，它采用四个样本并结合它们，具有神经网络的能力。该项目带有一组预编译和神经网络样本，[但你可以使用这个接口来混合你自己的样本](https://github.com/googlecreativelab/open-nsynth-super#audio-creation-overview)，前提是你有一台配备昂贵 GPU 的强大计算机。

不是要破坏这个项目的工作，但是成千上万的 synth 负责人会对这个项目感到失望。创建新的音频样本需要使用 GPU 进行训练；神经网络最难和计算最昂贵的部分是训练，而不是性能。没有一个好的显卡，你只能使用谷歌在这里提供的任何样本。

由于这是开源的，[所有文件都可用](https://github.com/googlecreativelab/open-nsynth-super)，而且这是一个使用带有激光切割外壳的 Raspberry Pi 的项目，因此对这款机器学习 Kaoss pad 有着巨大的需求。好消息是[在 Hackaday.io](https://hackaday.io/project/89396-open-nsynth-super) 上有一个团购，而且[已经在 Tindie](https://www.tindie.com/products/squarofumi/nsynth-super-pcb-googles-ml-synthesizer/) 上有一个卖家，如果你想要一个裸 PCB 的话。当然，你也可以自己卷，所有 SMD 零件的 Digikey cart 价格约为 40 美元。这还不包括有机发光二极管(来自中国的 2 美元)、树莓派或激光切割外壳，但这是一个开始。当然，对于那些没有通过 0805 SMD 焊接测试的人来说，看起来有几个人会以 50-60 美元的价格出售组装版本(不含 Pi)。

很酷吗？是的，但一个想把它添加到音轨中的受地下室束缚的制片人会很快发现，训练机器学习算法的成本远远高于玩机器算法。硬件很整洁，但是做好失望的准备。就像艾在 60 年代末 80 年代末遭受的。毕竟我们在人工智能复兴时期。

 [https://www.youtube.com/embed/iTXU9Z0NYoU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/iTXU9Z0NYoU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/0fjopD87pyw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/0fjopD87pyw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

