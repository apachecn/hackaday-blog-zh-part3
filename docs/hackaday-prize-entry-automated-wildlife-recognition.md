# Hackaday 奖参赛作品:自动野生动物识别

> 原文：<https://hackaday.com/2017/06/14/hackaday-prize-entry-automated-wildlife-recognition/>

如今，踪迹和野生动物相机随处可见，但是[野生眼](https://hackaday.io/project/24938)项目的目标不仅仅是拍摄生物的数码快照。[Brenda Armour]使用 Raspberry Pi 不仅拍摄游荡到相机视野中的野生动物的照片，还使用 IBM 的[视觉识别 API](https://www.ibm.com/watson/developercloud/visual-recognition.html) 通过 [Node-RED](https://nodered.org/) 基础设施自动识别和分类所看到的动物。结果是，当检测到运动时，系统捕获图像，将图像发送到视觉识别 API，并试图根据返回的数据识别任何野生动物。

视觉识别并非完美无缺，但最近的一项概念证明显示，成功识别乌鸦、猫和狗的结果令人鼓舞。也许当项目准备深入森林时，这些太阳能供电的网络鸟舍(也使用树莓派)的元素可以帮助减少一些绳索。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)