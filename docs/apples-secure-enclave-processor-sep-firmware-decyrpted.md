# 苹果公司的安全飞地处理器(SEP)固件解密

> 原文：<https://hackaday.com/2017/08/18/apples-secure-enclave-processor-sep-firmware-decyrpted/>

自称“arm 64 pornstar”[xerub]在网上发布了苹果安全飞地处理器(SEP)固件的[解密密钥。SEP 是 iPhone 5s 推出的安全协处理器，也是 touch ID 推出的时间。这是一个我们不应该知道的黑匣子，但[xerub]现在已经揭开了它的帷幕。](http://www.iclarified.com/62025/hacker-decrypts-apples-secure-enclave-processor-sep-firmware)

secure enclave 处理来自 touch ID 传感器的指纹数据，并确定它是否匹配，同时它还支持用户进行购买。SEP 是一个看门人，防止主处理器访问敏感数据。处理器发送只能由 SEP 读取的数据，SEP 通过从设备共享密钥生成的会话密钥进行认证。它也运行在自己的操作系统(SEPOS)上，该系统有一个内核、服务驱动程序和应用程序。SEP 为 SOC 的其余部分执行安全服务，您可以从 Blackhat 的[揭开安全飞地处理器讲座](https://www.youtube.com/watch?v=7UNeUT_sRos)中了解更多信息

【xerub】[在这里公布解密密钥](https://www.theiphonewiki.com/wiki/Greensburg_14G60_%28iPhone6,1%29)。要解密固件你可以使用 [img4lib](https://github.com/xerub/img4lib) 和 xerub 的 [SEP 固件拆分工具](https://gist.github.com/xerub/0161aacd7258d31c6a27584f90fa2e8c)来处理。这些工具使安全研究人员在固件中查找漏洞变得轻而易举。