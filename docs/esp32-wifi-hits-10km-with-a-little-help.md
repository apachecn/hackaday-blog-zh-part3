# ESP32 WiFi 只需一点帮助就能达到 10 公里

> 原文：<https://hackaday.com/2017/04/11/esp32-wifi-hits-10km-with-a-little-help/>

[Jeija]正在玩一些 ESP32s，在真正的黑客时尚中，他想知道他能把它们分开多远，同时还能让数据流动。他的[视频对这个问题的回答](https://www.youtube.com/watch?v=yCLb2eItDyE)涵盖了 Friis 方程，并有许多使用该方程的好例子，分贝，甚至还有一个覆盖约 10km 的实际例子。你可以看下面的视频。

当然，要获得这样的范围，你需要一个定向天线。为了避免违反控制发射功率的规定，他在接收端使用天线。这也意味着他不得不侵入 ESP32 WiFi 堆栈，使设备只能在一边监听。黑客将设备置于混杂模式，只监控正在发送的信号。你可以在 [GitHub](https://github.com/Jeija/esp32free80211) 上找到相关代码(包括一个 rickrolling 应用程序)。

当然，天线并不新鲜——看看我们过去见过的所有 Pringle can 天线。然而，使用远程只接收模块很有意思，我们可以看到这种技术在远程无人机视频或遥测以及驾驶方面的应用。如果你周围没有大型天线，你可以试试胶带。如果你想要更详细的分贝复习，我们[上个月做了](https://hackaday.com/2017/03/07/saved-by-the-bel-understanding-decibels/)。

 [https://www.youtube.com/embed/yCLb2eItDyE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/yCLb2eItDyE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

