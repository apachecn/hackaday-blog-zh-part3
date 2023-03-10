# 掌握生物识别技术

> 原文：<https://hackaday.com/2015/09/20/getting-biometrics-in-hand/>

令人惊讶的是，只要你把钥匙带在身上，你很快就能适应一辆启动的汽车。当你换车时，把钥匙拿出来插在点火装置上是一件麻烦的事。生物识别旨在让它变得更简单。如果计算机可以唯一识别你，为什么要随身携带钥匙(或门禁卡)？

[Alexis Ospitia]想要试验静脉匹配生物识别技术，并且[用树莓 Pi、网络摄像头和定制红外照明系统](http://www.instructables.com/id/Biometria-de-las-venas-de-la-mano-Raspberry-Pi-LCD-1/)获得了良好的结果。显然，血红蛋白是一种良好的红外反射体，你手上的静脉图案与其他生物特征一样独特(如指纹、耳纹和视网膜静脉图案)。[Alexis 的]帖子是西班牙语的，但是[谷歌翻译](https://translate.google.com/translate?sl=es&tl=en&js=y&prev=_t&hl=en&ie=UTF-8&u=http%3A%2F%2Fwww.instructables.com%2Fid%2FBiometria-de-las-venas-de-la-mano-Raspberry-Pi-LCD-1&edit-text=&act=url)做得很好，只要你意识到它认为“指纹”是“足迹”该软件使用 OpenCV，但我们已经看到在 MATLAB 中做了同样的事情(见下面的视频)。

指纹扫描仪看起来很有前途，但也有人担心。他们很容易被欺骗，如果他们不够成熟，他们就会受到字面上的攻击(我们不希望有人拿着一把断线钳潜伏在 ATM 机周围)。我们认为一只断手不会有足够的血来骗过这个系统，但是我们不愿意验证这个理论。

有一些商业系统使用了来自 Fijitsu、Toshiba 和其他公司的类似技术。我们不得不怀疑是否有其他地方你可能有独特的静脉模式，这将是有用的扫描。我们之前已经讨论过[指纹扫描仪](http://hackaday.com/2014/06/25/fingerprint-scanner-both-simplifies-and-complicates-opening-garage-door/)，虽然我们已经报道过[有人假冒手持扫描仪](http://hackaday.com/2008/08/14/defcon-16-biometric-cloning/)，但我们不认为这种方法适用于这种特殊的设置。

 [https://www.youtube.com/embed/sw-NiQPDeao?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/sw-NiQPDeao?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

