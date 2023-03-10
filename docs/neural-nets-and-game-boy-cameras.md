# 神经网络和游戏机相机

> 原文：<https://hackaday.com/2017/02/20/neural-nets-and-game-boy-cameras/>

发布于 1998 年的 Game Boy camera 可能是许多年轻黑客拿到的第一台数码相机。大约在索尼 Mavica 相机将 VGA 分辨率的图片放到软盘驱动器上的时候，Game Boy 相机正在拍摄 256×224 分辨率的图片，并在 190×144 分辨率的显示器上显示它们。画面质量很糟糕，但[罗兰·梅尔滕斯]最近有了一个想法。[为什么不使用神经网络将这些 Game Boy 相机图片变成照片般逼真的图像](http://www.pinchofintelligence.com/photorealistic-neural-network-gameboy/)？

神经网络、深度学习、机器学习或我们使用的任何其他时髦词汇都需要训练数据。在这种情况下，训练数据将是来自 Game Boy 相机的图片和同一场景的全色、高分辨率图像。这个数据集显然不存在，所以[Roland]拍摄了一些名人的特写镜头，并将颜色减少到四种灰色。

[![[Roland]'s face captured with the Game Boy Camera (left), and turned into a photorealistic image (right)](img/2c56aca7761d20b099fa7c773c0fd07a.png)]([) 

【罗兰】用 Game Boy 相机抓拍的人脸(左)，变成了照片般逼真的图像(右)

对于本次实验的深度机器人工神经学习部分，【罗兰】翻到了几张关于将[照片转换成草图](https://arxiv.org/pdf/1606.03073v1.pdf)再转换回来的论文，[实时风格传递](https://arxiv.org/pdf/1603.08155v1.pdf)。经过一些工作后，这个神经网络将测试数据转换回与原始图像相当相似的图像。这是你会从一个经过训练的神经网络中期待的，但[Roland]也通过这个深度机器人工学习 minsky 从 Game Boy Camera 发送了几张图片。这些图像出人意料地好——有点褪色，但几乎符合人物性格。

这些年来，我们已经看到了很多针对游戏机摄像头的黑客攻击。从[用微控制器](http://hackaday.com/2016/03/08/game-boy-camera-cartridge-reversed-photos-dumped/)转储原始图像到[将传感器变成摄像机](http://hackaday.com/2015/11/03/gameboy-camera-becomes-camcorder/)的一切都已经完成。虽然[Roland]的技术只能在人脸上工作，但它是神经网络所能做的一个很好的例子。