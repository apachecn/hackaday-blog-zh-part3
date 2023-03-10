# 黑客字典:超声波通信

> 原文：<https://hackaday.com/2016/04/15/hackaday-dictionary-ultrasonic-communications/>

假设你有一个正在制作的精巧的小工具。您需要向它发送数据，但您希望保持简单。你可以增加一个 WiFi 接口，但那会消耗能量。[蓝牙低能耗](http://hackaday.com/2015/12/02/hackaday-dictionary-bluetooth-low-energy/)功耗更低，但会变得复杂，如果你只是想发送少量数据，这就有点过头了。如果您的设备有麦克风，还有一种方式您可能没有考虑到:超声波通信。

使用高于人类听觉极限的声音频率的想法有许多优点。大多数设备已经有能够发送和接收超声波信号的扬声器和麦克风，因此不需要额外的硬件。超声波的频率超出了人类听觉的范围，所以通常是听不到的。它们还可以与标准音频一起传输，因此不会干扰媒体设备的功能。

许多小工具已经使用这种类型的通信。谷歌 Chromecast HDMI 加密狗可以使用它，在发送到电视的音频输出上叠加一个超声波信号。它利用这一点，通过超声波发送一个 4 位数的代码来与访客设备配对，该代码授权访客设备加入 ad-hoc WiFi 网络并向其传输内容。这个想法是，如果设备不能接收超声波信号，它可能没有被邀请参加聚会。

不久前，我们报道了[Chris]使用 GNU Radio 实现超声波数据的[。他的](http://hackaday.com/2013/12/10/ultrasonic-data-transmission-with-gnu-radio/)[文章详细介绍了他如何设置系统，并展示了一个使用笔记本电脑扬声器和麦克风的简单演示。他使用频移键控(FSK)将数据编码到音频中，使用 23Khz 的基频，并以五个字节的数据包发送数据。](https://www.anfractuosity.com/projects/ultrasound-via-a-laptop/)

 [https://www.youtube.com/embed/H0DKRl8XIcU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/H0DKRl8XIcU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



从那以后，[Chris]扩展了他的系统,创建了一个双向系统，两个设备使用不同的频率进行双向通信。为了提高可靠性，他还将调制方案改为高斯频移键控，甚至在上面添加了虚拟驱动层，因此该连接可以传输 TCP/IP 流量。是的，他建立了一个超声波网络连接。

不过，他的实现凸显了这种数据传输方式的一个问题:速度慢。数据传输的速度受到系统传输和接收数据能力的限制，而且[Chris]发现他需要保持较慢的速度才能使用廉价的麦克风和扬声器。具体来说，他必须保持 GFSK 调制所使用的每个符号的样本数很高，从而给接收机更多的时间来发现数据流中每个符号的频移。这可能是因为扬声器和麦克风不是专门为这种频率设计的。系统还要求在每个数据包之前有一个前同步码，这增加了连接的等待时间。

所以超声波通信可能不快，但比 WiFi 或其他射频信号更难拦截。尤其是当你没有在寻找它们的时候，这启发了黑客[Kate Murphy]创建了 [Quietnet](https://github.com/Katee/quietnet) ，一个简单的 Python 聊天系统，它使用 [PyAudio](http://people.csail.mit.edu/hubert/pyaudio/) 库来发送超声波聊天消息。为了额外的安全，该系统甚至允许你改变载波频率，这可能是有用的，如果联邦调查局盯上了你。无论是公开的、隐蔽的，还是仅仅为了简单的硬件配置，超声波通信都是可以考虑使用的，并且可以添加到您的硬件技巧包中。