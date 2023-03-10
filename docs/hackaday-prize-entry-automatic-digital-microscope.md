# Hackaday 奖参赛作品:自动数字显微镜

> 原文：<https://hackaday.com/2016/06/10/hackaday-prize-entry-automatic-digital-microscope/>

泽赫尔-尼尔森痰涂片镜检是诊断结核病最常用的方法之一。在设备方面，它只需要一个光学显微镜，尽管它仍然需要一个训练有素的专业人员透过玻璃观察，识别和计数样本中的细菌数量。为了向缺乏设备和训练有素的人员的地区提供可靠有效的结核病诊断，[Rodrigo Loza]和[khalilnallar]正在开发一种基于计算机视觉和机器学习的自动数字显微镜[，这是他们获得 Hackaday 奖的参赛作品。](https://hackaday.io/project/10188-automatic-digital-microscope)

[![automated_microscope_detection_1](img/c1e255b16dee74a92e0fff9d0ca67be3.png)](https://hackaday.com/wp-content/uploads/2016/06/automated_microscope_detection_1.png) 他们开始从互联网上收集结核细菌的图像，并试验了检测染色细菌的颜色阈值算法，以及计算细菌个体和集群的算法。据该团队称，仅这一过程就需要一名训练有素的专业人员花费 30 分钟或更长时间。图形界面突出显示已识别的细菌并读取细菌计数。

[Rodrigo Loza]和[khalilnallar]正在玻利维亚科比亚的罗伯托·加林多·特兰医生医院测试他们的设备。然而，获得实验室环境是一回事，获得稳定供应的新鲜结核分枝杆菌样本是另一回事。由于无法获得在活体上测试算法所需的样本，他们转向了项目的另一个前沿:硬件。经过几次迭代，他们开发了一种低成本、3D 可打印的套件，可以将实验室级光学显微镜转变为嵌入式 CNC 控制的显微镜平台。他们的套件包括三个基于步进电机的 X、Y 和 Z 轴，以及一个网络摄像头支架。一个英特尔 Edison 和一个定制的 Arduino 兼容屏蔽控制系统，以实现诸如寻的程序、自动对焦和细菌检测等功能。

该团队目前正在完善他们的细菌检测管道，探索半自动检测方法、机器学习和神经网络在硬件限制内对细菌进行分类的可行性。下面的视频显示了他们显微镜 Z 轴的最新更新。

 [https://www.youtube.com/embed/M3xv8q6CFng?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/M3xv8q6CFng?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2016](http://hackaday.io/prize) is Sponsored by: [![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](http://hackaday.io/atmel)  [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](http://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](http://www.digikey.com/)  [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](http://supplyframe.com/)