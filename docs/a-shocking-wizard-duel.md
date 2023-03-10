# 一场令人震惊的巫师决斗

> 原文：<https://hackaday.com/2017/07/04/a-shocking-wizard-duel/>

你可能听说过亚瑟·C·克拉克第三定律，该定律表明任何足够先进的技术都与魔法无异。从字面上和最好的角度来看，[足够先进]的[艾伦·潘]正在使用现成的技术来模拟哈利·波特式的魔法决斗。

名为“巫师模拟非魔法决斗模拟器”或简称为 w . a . n . d . s——是一个更具互动性的激光枪战版本。它特别吸引人，因为你的身体在这条线上。一个使用谷歌语音识别服务的树莓派会听到咒语的名字，记住，发音是关键，它会从一个红外 LED 魔杖发出咒语。每个决斗士都有五个法术可以使用，但是他们的准确度取决于你。

一旦对手的接收器记录到击中，Arduino 就会触发经皮神经电刺激(TENS)设备，向身体的各个部位发送脉冲，以模拟咒语的效果。巫师之间的几次电击算什么，嗯？

作为对持续弹幕的防御，法术 Protego——针对自己的传感器——给予几秒钟的免疫；然而，所有的法术都有一个内置的冷却系统来防止它们被滥用，魔杖上的 LED 会指示它们何时可以使用。

 [https://www.youtube.com/embed/SQApEHUKK2g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/SQApEHUKK2g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



这一点技术魔法的代价是，当语音识别退出并到达服务器进行处理时，咒语在生效前会有一点滞后。所以这还不是快节奏的决斗——现在还不是！

很久以前，另一种巫师在地下活动。今天，他们中至少有一个人正在利用新的印刷技术来保持他们的热情。

[via[RaspberryPi.org](https://www.raspberrypi.org/blog/real-life-wizard-duel/)