# 记录功能肌肉帮助脊髓损伤患者康复

> 原文：<https://hackaday.com/2017/01/10/recording-functioning-muscles-to-rehab-spinal-cord-injury-patients/>

[迭戈·马里尼奥]和他在都灵理工大学(Politecnico di Torino，意大利都灵理工大学)的同事设计了一个原型，可以让患有运动障碍的患者，如脊髓损伤(SCI)的患者，通过功能性电刺激进行[康复。他们设计了一个系统，记录并解释来自理疗师的肌肉信号，然后通过电刺激器刺激患者体内的特定肌肉。](http://systemforinducingmovement.blogspot.pt/2016/11/system-for-inducing-movement-in.html)

该采集系统基于 BITalino 板，当理疗师执行为患者康复计划设计的特定锻炼时，该板记录来自其肌肉的表面肌电图(sEMG)信号。BITalino 使用蓝牙将数据发送到 PC，在那里数据在 Matlab 中进行适当的处理，以便识别和分离肌肉活动模式。

之后，信号通过连接到 Globus Genesy 600 电刺激器的中继板在病人身上“重放”。这个中继板黑客主要是因为 Globus Genesy 是不可编程的，所以这是他们实现刺激器的快速方法。在他们的视频中，我们可以看到，在“理疗师”完成动作后，肌肉活动立即被回放。这显然是一个原型，但它确实显示了有希望的结果。

[https://drive.google.com/file/d/0B8Kznl9S3-NoNDRmTkFFU0l1T1E/preview](https://drive.google.com/file/d/0B8Kznl9S3-NoNDRmTkFFU0l1T1E/preview)

它让我们想起了[肌电手](http://hackaday.com/2016/05/26/hackaday-prize-entry-open-source-myoelectric-hand-prosthesis/)，而不是人类。不久前，我们为那些对这个话题感兴趣的人特别推出了一个 [EMG 教程](http://hackaday.com/2016/11/20/emg-tutorial-lets-you-listen-to-your-muscles/)。在不从优秀和必要的医学研究中获益的情况下，我们都在等待有一天，我们所有的生物信号都可以被容易地读取和翻译成，比如说，像[方法-2](http://hackaday.com/?p=238513) 这样的巨大化身机器人。对吗？对吗？…