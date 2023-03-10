# AI 看着你睡觉；知道你什么时候做梦

> 原文：<https://hackaday.com/2017/08/29/ai-watches-you-sleep-knows-when-you-dream/>

如果你从未在睡眠实验室做过病人，那么在一个人睡觉时对其进行监测是一个涉及到电线、传感器和不适的复杂过程。为了寻找一种更好的方法，麻省理工学院的研究人员——由[Dina Katabi]领导，并与马萨诸塞州总医院合作——开发了一种设备，可以非侵入性地识别患者的睡眠阶段。

该设备大约有笔记本电脑大小，安装在患者附近的墙上，可以测量反射的低功率射频信号的微小变化。无线信号由深度神经网络人工智能进行分析，并预测患者的各种睡眠阶段——浅睡眠、深睡眠和快速眼动睡眠——从而消除了手动梳理数据的任务。尽管该设备很敏感，但它能够过滤掉无关的运动和干扰，专注于患者的呼吸和脉搏。

这里的新颖之处与其说是硬件，不如说是处理方法。研究人员使用卷积和递归神经网络以及他们所谓的对抗性训练机制:

> 我们的训练方案涉及 3 个参与者:特征编码器(CNN-RNN)、睡眠阶段预测器和源鉴别器。编码器与预测器进行合作博弈以预测睡眠阶段，并与源鉴别器进行最小最大博弈。我们的源鉴别器不同于标准的域对抗鉴别器，因为除了编码特征之外，它还将睡眠阶段的预测分布作为输入。这种相关性有助于说明阶段和个体之间的内在相关性，如果不降低预测任务的性能，就无法消除这种相关性。

有人想在家里试一试吗？我们很乐意看到 HackRF 和 GNU 无线电用来记录 RF 数据。研究人员将 RF 与 WiFi 进行了比较，因此重新利用 2.4 GHz 无线电来发送重复的统一传输是一个好的开始。[将它转储到 TensorFlow](http://hackaday.com/2017/04/11/introduction-to-tensorflow/) 中并报告回来。

 [https://www.youtube.com/embed/ltcjly-CYkI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ltcjly-CYkI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



该团队希望让睡眠障碍的诊断变得更容易，以及其他扰乱睡眠的疾病，如阿尔茨海默氏症和帕金森氏症。该团队声称准确率高达 80%,并认为这可以与使用脑电图和技术人员监测睡眠周期的传统方法相媲美——对所有相关人员来说麻烦要少得多。

尽管如此，有时需要采取极端措施来劝阻外界力量打扰你的睡眠，或者寻求可爱的终结者 T2 的帮助。

[感谢您的提示，我通过 [Gizmodo](http://gizmodo.com/wi-fi-signals-may-one-day-be-used-to-tell-if-you-re-dre-1797728021) 发送]