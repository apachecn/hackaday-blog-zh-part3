# 用激光雷达数字化你的房间

> 原文：<https://hackaday.com/2017/05/15/digitize-your-room-with-lidar/>

想象一个房间的最佳方式是什么？一张照片？哈——不要这么守旧！你想要一个[激光雷达装备](http://kurokesu.com/main/2017/05/08/3d-scanning-like-a-pro/)来扫描空间，并在你的计算机中将其重建为 3D 点地图。

紧随[Saulius Lukse]的[扫描温度计](http://hackaday.com/2017/05/02/thermal-panorama-one-pixel-at-a-time/)之后，他用飞行时间(TOF)相机(Garmin LIDAR)取代了他们云台设置上的热感相机，该相机每秒能够扫描 500 个样本，只需 15 分钟就能扫描完他们的房间。位置数据与测距信息相结合，使用 Python 生成点云。在 3D 操作程序中打开该文件，您会看到这样一幅画面:

[![](img/16f910e6b90b3ffa148904543a7b2cc8.png)](https://hackaday.com/wp-content/uploads/2017/05/result2_2d.png)

这是由 470 万个点云生成的图像。它并不完美，但肯定可以。

[Lukse]遗憾地说，这种相机需要理想的照明条件，这使它不适合大量的室外成像，而且同样局限于较短的范围。这还需要随身携带一台笔记本电脑，所以他正在考虑将它做成一个一体化的包。

想了解激光雷达的工作原理吗？看看这个警察测速激光雷达“枪”的拆卸视频。或者看看这个[(速度更快)完全 DIY 的激光扫描仪](http://hackaday.com/2016/06/05/in-soviet-russia-diy-laser-rangefinder-scan-you/)。