# 大脑:用 NASB 的声音破解手机密码

> 原文：<https://hackaday.com/2017/04/01/cerebrum-mobile-passwords-lifted-acoustically-with-nasb/>

有数不清的密码黑客方法，但声学和加速度计传感方面的最新进展为旁道攻击打开了大门，密码或其他敏感数据可以从设备的电子设备和人机界面的声学属性中提取出来。最近一个戏剧性的例子包括[通过监听](http://hackaday.com/2013/12/20/ambient-computer-noise-leaks-your-encryption-keys/)处理器在处理数字时发出的声音频率来破解 RSA 加密。

现在有一个新的远程黑客登场了。Cerebrum 系统代表了侧信道密码攻击的最新创新，利用移动和其他电子设备的声学特征在远距离提取密码数据。

cFREG 的研究科学家提供了一个令人信服的大脑原型演示。它使用密码频率感应(PFS)，即获取输入电子设备的密码的声音签名，发送到云，通过专有的深度学习算法，并进行解码。演示和技术细节显示在下面的视频中。

 [https://www.youtube.com/embed/ZxUbKsrxrOg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZxUbKsrxrOg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



正如麻省理工学院研究员 T. M. Gil 在他标志性的[论文](https://pdos.csail.mit.edu/archive/scigen/steeve.pdf)中所解释的那样，这些方法中的许多已经被展示过了，

近年来，许多研究致力于探索冯·诺依曼机；然而，很少有人部署模拟退火的研究。事实上，很少有安全专家会不同意对在线算法的调查[25]。STEEVE 是我们新的博弈论模式系统，是应对所有这些挑战的解决方案。”

为了反驳这种观点，cFREG 的研究人员将它提升到了一个更高、更准确的水平。

## 衡量

Cerebrum 团队从原型系统开始工作，以增加他们设备的范围。第一步是表征声学模拟前端和传感器，特别注意非正统的声学聚焦元件:

![](img/b94ebb9681b332bbb133e545c73ccdcb.png)

这些改进是基于使用现成棉花糖的净空气糖边界(NASB)的比率。温度探测对于校准这种性能是不可或缺的，随着这一成功，他们继续对远程系统进行现场测试。

## 扩大范围

通过同轴电缆到棉花糖的过渡，将磁性环形天线直接连接到大脑上，对原型进行了测试。通过带着低姿态环形天线走在街上，许多密码被成功检测和解码。

 [![Coax to marshmallow transition.](img/3db6baa451d1facbeb4f80d6b0007891.png "Coax to marshmallow transition.")](https://hackaday.com/2017/04/01/cerebrum-mobile-passwords-lifted-acoustically-with-nasb/interfacing-feed-line-into-cerebrum/)  [![Detecting and decoding passwords.](img/717ffd34b6b42f6bd5b9be263ba37a89.png "Detecting and decoding passwords.")](https://hackaday.com/2017/04/01/cerebrum-mobile-passwords-lifted-acoustically-with-nasb/loop-antenna-on-the-street/) 

## 使用 PFS 进行战争驾驶

为了最大限度地扩大范围，增加了额外天线孔径，并安装在一个移动平台上，包括一个对数周期天线、一个 X 波段抛物面天线和一个磁环天线，以捕捉任何和所有低频数据。在这种配置中，有可能从离车辆一英里以上的地方收集大量的密码，从而形成一个密码宝库。

 [![PFS war wagon.](img/25ba2365c5b45228db3ce4b87e9e5869.png "PFS war wagon.")](https://hackaday.com/2017/04/01/cerebrum-mobile-passwords-lifted-acoustically-with-nasb/pfs-war-wagon/)  [![Cerebrum in the war wagon.](img/5a437ca1cbc5db08caae4da68964542c.png "Cerebrum in the war wagon.")](https://hackaday.com/2017/04/01/cerebrum-mobile-passwords-lifted-acoustically-with-nasb/cerebrum-in-war-wagon/) 

![](img/e706734faabbda738af1ddf349fbba72.png)

无需太多努力，Cerebrum PFS 的最大范围和整体性能就得到显著提高，从而开辟了大量的额外应用。这是一个现存的令人不安的漏洞。但是研究人员有一个推荐的解决方案，当处理用户输入时，在移动设备中实现无意义的计算。产生的错误声音将足以欺骗机器学习算法…目前来说。