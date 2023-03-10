# 婴儿监视器重建也是 ESP8266 音频流如何

> 原文：<https://hackaday.com/2016/07/15/baby-monitor-rebuild-is-also-esp8266-audio-streaming-how-to/>

[Sven337]重建了一个便宜又糟糕的婴儿监视器并不是超级视觉化的，但是它比第一眼看上去要复杂得多。它还介绍了如何使用一对 ESP8266 设备通过 UDP over WiFi 传输音频流，并坦率地分享了在此过程中出现的问题以及如何解决这些问题。[Sven337]甚至试验了几种不同的方法来实时压缩传输的音频数据，没有别的原因，只是为了在不增加部件或花费额外资金的情况下尽可能地做好事情。

[![receiver](img/77444175acab763889bb70d8cef5ca4e.png)](https://hackaday.com/wp-content/uploads/2016/07/receiver.jpg) 最初的婴儿监视器有音频和视频，但是[因为一些原因完全没有用](https://perso.aquilenet.fr/~sven337/francais/2016/04/10/Analyse-dun-babyphone-pourri.html)(法语)。范围和质量都很糟糕，音频充满了静电干扰，就像麦克风实际从房间里拾取的任何东西一样大。用户只有两种选择:要么让白噪声不断地从接收器中传出，要么因为你调低了音量以消除持续的静电干扰而听不到你的孩子。我们最喜欢的部分是 VOX“功能”:如果婴儿很安静， *它会关闭接收器的屏幕*；这对音频没有任何影响！锦上添花的是，模拟 2.4GHz 发射器在发射时会干扰家庭 WiFi 这是一直存在的，因为它始终是打开的。

难怪 Sven337 决定走 DIY 路线。这个单位没有被扔进垃圾桶，而是几乎从头开始重建。

[![inside_full_2](img/66532fc3a1f58877ccb3ccd5b218ed8d.png)](https://hackaday.com/wp-content/uploads/2016/07/inside_full_2.jpg) 重复使用机箱意味着 DIY 重建看起来和实际一样好。毕竟，[Sven337]不想在托儿所里干粗活。但是不要让围栏内丑陋的混乱*欺骗了你——在这个建造中有很多细节工作。内部可能是杂乱的电线和分线板，但在将项目安装到其他设备的外壳中的空间限制内工作通常是一个挑战。*

ESP8266 可以工作，但并不完全适合音频婴儿监听器，因为它缺乏高质量的 ADC 和 DAC。但另一方面，它很便宜，很容易使用，并且有足够的处理能力。这些特性是 ESP8266 进入如此多项目的原因，包括像[这个 WiFi 网络摄像头](http://hackaday.com/2016/01/24/truly-versatile-esp8266-wifi-webcam-platform/)这样的家用设备。