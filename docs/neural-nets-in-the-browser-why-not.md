# 浏览器中的神经网络:为什么不？

> 原文：<https://hackaday.com/2017/08/04/neural-nets-in-the-browser-why-not/>

我们不断看到越来越多的张量流神经网络项目。我们也不断看到越来越多的东西在浏览器中运行。你不必是史波克先生也能预见到这一次的到来。TensorFire 在浏览器中运行神经网络，并声称 WebGL 允许它像在用户的桌面计算机上一样快地运行。主页是一个风格化图像的演示，但如果你想了解更多细节，你可能会想访问[项目页面](https://tenso.rs/#readmore)。你也可能会喜欢下面的视频，它来自创作者之一的郭凯文。

TensorFire 有两个部分:一个用于编写在 4D 张量上操作的大规模并行 WebGL 着色器的低级语言，以及一个用于从 Keras 或 TensorFlow 导入模型的高级库。作者声称，它可以在任何 GPU 上工作，在某些情况下，实际上比运行原生 TensorFlow 更快。

这是使用 [WebGL 进行基于浏览器的并行处理](http://hackaday.com/2017/07/17/using-the-gpu-from-javascript/)的逻辑进展，我们之前已经介绍过了。这项工作是由一群最近从麻省理工学院毕业的学生完成的，他们为自己的工作申请了(并获得了)T2 人工智能资助。我们想知道一些有事业心的 Hackaday 读者是否可能得不到类似的融资(注意，你必须在 8 月底前申请)。

如果你一直渴望了解更多关于 TensorFlow 的知识，我们已经对它进行了深入的报道。如果你想要[的基本例子](http://hackaday.com/2017/03/14/google-machine-learning-made-simpler/)，我们也已经看过了。

 [https://www.youtube.com/embed/omadDmoinrc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/omadDmoinrc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢[帕特里克]的提示。