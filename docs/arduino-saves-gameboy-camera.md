# Arduino 拯救 Game Boy 相机

> 原文：<https://hackaday.com/2017/12/01/arduino-saves-gameboy-camera/>

[Brian Khuu]在网上买了几个 Game Boy 相机，发现上面还有以前主人的照片。相机里的内存有备用电池，如果电池没电了，照片就会成为历史，所以他决定发起一场营救行动。

他知道 Game Boy 如何与配套的袖珍打印机对话的协议是可用的，所以他使用 Arduino 和网络浏览器来提取照片。如果你想保存你的照片，结果代码在 [GitHub](https://github.com/mofosyne/arduino-gameboy-printer-emulator) 上。虽然[布莱恩]不需要破解协议，但他确实对此提供了一个很好的解释。甚至还有一些嗤之以鼻的展示。Arduino 负责所有的通信，并欺骗游戏，让它以为自己是配套的打印机。然而，它只是将数据流式输出，Javascript 解码器处理实际的解码。事实上，在博文中，你可以输入数据，点击一个按钮，然后看到最终的游戏男孩图片。

它工作了，但是[布莱恩]确实遇到了一些问题。首先，这些设备似乎没有使用任何流量控制，所以他别无选择，只能跟上游戏机。此外，还有一个他无法正确解码的 CRC。然而，这些照片看起来不错——至少和 Game Boy 的照片看起来一样好。所以他确实得到了结果。

在之前，我们已经看到[在 PC 上完成。如果你对反过来更感兴趣，顺便说一句，你可以用一台真正的 Game Boy 打印机从一台 Arduino](https://hackaday.com/2016/03/08/game-boy-camera-cartridge-reversed-photos-dumped/) 上[打印。](https://hackaday.com/2013/12/17/fubarino-contest-game-boy-printer/)