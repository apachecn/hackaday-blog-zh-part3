# 摄影测量的超详细 3d 扫描

> 原文：<https://hackaday.com/2016/02/03/super-detailed-3d-scans-with-photogrammetry/>

摄影测量是一个真实的词，shapespeare 为自己建造了一个很好的装置，用它来进行高分辨率的 3d 扫描。摄影测量的一组好的图像是:清晰的焦点，良好的照明，精确的索引，并有统一的背景。背景由一个 [3d 打印台](https://www.thingiverse.com/thing:548006)和一些复印纸处理。为了获得均匀的照明，他使用了四盏宜家可调 LED 灯。

为了精确地索引物体，他用 Arduino 和步进电机建立了一个索引设置(安装在自称是最优雅的 3d 打印外壳中)。Arduino 旋转平台一个测量的增量，然后使用[Sebastian Setz]的[非常简洁的红外相机控制库](http://sebastian.setz.name/arduino/my-libraries/multi-camera-ir-control/)，拍摄照片。重复这个过程，直到拍摄了物体的多张照片。

一旦照片被拍摄，他们需要通过摄影测量处理器运行。[shapespeare]使用的是 [Agisoft Photoscan](http://hackaday.com/2014/03/07/an-affordable-full-body-studio-grade-3d-scanner/) ，但他说 [Autodesk Memento](https://memento.autodesk.com/about) 和 [123d Catch](http://hackaday.com/2014/07/08/break-your-frames-print-some-new-ones/) 也做得很好。在所有这些工作之后，似乎[shapespeare]使用他的新能力 3d 打印了一个巨大的甲板螺钉。酷毙了。