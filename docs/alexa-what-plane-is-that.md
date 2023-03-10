# “Alexa，那是什么飞机？”

> 原文：<https://hackaday.com/2017/07/02/alexa-what-plane-is-that/>

我们可能都做过这样的事——凝视着一架经过的喷气式飞机，想知道它要去哪里，乘客们开始了什么样的冒险。虽然后者很难回答，但前者变得简单了一点:[只要问 Alexa 飞机是什么](https://www.nicksypteras.com/projects/teaching-alexa-to-spot-airplanes)。

诚然，[Nick Sypteras]的 Echo Dot 并不全知，不足以确切知道你在看什么飞机。他的系统受益于他波士顿公寓的窗户提供的限制——从下面的视频中，我们猜测在比肯山或伦敦西区的某个地方——提供了洛根机场的入口。一个 RTL-SDR 加密狗接收来自附近所有飞机的 ADS-B 传输，一个 Raspberry Pi 进行查找，选择最近的飞机，并从 FlightRadar24 搜索出发和到达机场。Alexa 做剩下的，但我们不得不承认听到“波音 787”而不是“787”会让我们发疯。

如果你对机场的视野不够开阔，无法让[尼克]的黑客技术发挥作用，也许[一台飞机定位机器人摄像机](http://hackaday.com/2014/11/27/keep-tabs-on-passing-jets-with-pi-and-sdr/)会对你更好。

 [https://www.youtube.com/embed/j4wkChX5lXg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/j4wkChX5lXg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[via[RTL-SDR.com](http://www.rtl-sdr.com/asking-an-amazon-echo-to-spot-planes-with-help-from-an-rtl-sdr-and-raspberry-pi/)