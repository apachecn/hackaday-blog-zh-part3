# LTE IMSI 捕捉器

> 原文：<https://hackaday.com/2017/05/30/lte-imsi-catcher/>

GSM IMSI 捕手利用了 GSM 协议中的一个加密错误。但是我们现在有 LTE，为什么要担心呢？没人有 LTE IMSI 捕手吧？不对。[Domi]在这里有一个软件定义的基站收发器，它将比你说“黄貂鱼”更快地[捕捉你的 IMSI](https://www.youtube.com/watch?v=WXBk0XZqGf8)。

首先，什么是 IMSI？IMSI 代表国际移动用户身份。如果 IMEI(国际移动设备身份)是你的车牌，你的 IMSI 就是你的驾照。IMEI 是特定于手机的。您的 IMSI 用于识别您的身份，允许电话公司验证您的原籍国和移动网络订阅。

现在，带着术语,[多米]是如何偷走你的 IMSI 的？四个字:跟踪区域更新请求。当 LTE 网络上的电话接收到跟踪区域请求时，LTE 协议要求电话在可以重新连接到基站之前删除其所有认证信息。身份验证不存在[Domi]欺骗一个塔，等待电话连接，请求电话的 IMSI，然后拒绝电话的身份验证请求，所有这一切都在电话用户的眼皮底下进行。

现在，在你戴上锡纸帽子之前，请允许我们提出一些更有效的建议。需要更多手机相关的黑客？[我们支持你。](http://hackaday.com/category/cellphone-hacks/)

 [https://www.youtube.com/embed/WXBk0XZqGf8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/WXBk0XZqGf8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

