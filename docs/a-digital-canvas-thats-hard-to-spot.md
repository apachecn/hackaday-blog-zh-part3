# 很难发现的数字画布

> 原文：<https://hackaday.com/2016/01/19/a-digital-canvas-thats-hard-to-spot/>

虽然非常缺乏这张数字画布内部的图片，但我们对制作如此令人信服的物体的工作印象深刻。[Clay Bavor]想要一个数码相框，但在市场上找不到他想要的。他们都有类似的问题，液晶显示器质量最差，它们装在廉价的挡板里，它们有着[的怪异特征](http://hackaday.com/2012/07/12/digital-picture-frame-that-rotates-to-match-image-orientation/)，它们没有视角，它们要么像太阳一样发光，要么在黑暗的环境中看不见。

[Clay]从液晶显示器的质量开始，他查看了绝对最佳显示器的液晶显示器规格，然后大概意识到他生活在一个金钱不成问题的世界，于是买了一台 27 英寸的 iMac。iMac 的像素密度非常高，没有可视角度，苹果公司需要解决每个显示器的色彩平衡问题。接下来，他为 iMac 弄了一个真正的框架，在墙上挖了一个洞来容纳它，还安装了一个垫子来裁剪显示器，使其具有更令人信服的艺术纵横比。该构建最有趣的部分之一是添加了 Phidgets 光传感器。利用这一点，他运行了一些软件，不断调整 Mac 的亮度，使其在房间的灯光下几乎感觉不到。

一旦他把它做好了，他就开始摆弄他为框架编写的软件。因为他想让相框看起来像真正的艺术印刷品，所以他不能在人们看着的时候改变图像，所以他使用 Mac 上的摄像头和面部检测来确保图像只在没人看的几分钟内改变。他还有一种模式，当用户看向别处时，通过改变图像来欺骗用户。

我们承认，一个更黑客的版本是从一台坏掉的 iMac 上撕下面板，用一台重量更轻的电脑来运行所有的显示内容。[Clay]也得出了相同的结论，并计划为他的 2.0 版本做类似的事情。

【via [黑客新闻](https://news.ycombinator.com/item?id=10900439)