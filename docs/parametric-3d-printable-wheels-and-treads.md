# 参数化 3D 可打印车轮和轮胎面

> 原文：<https://hackaday.com/2016/11/28/parametric-3d-printable-wheels-and-treads/>

谈到机器人平台，有一个永恒的问题:轮子。轮子有无限多种用途，但是如果你买一个轮式机器人底盘，你只有一个选择。即使你去当地的恐怖货运，也只有大约五六种不同的车轮可用，所有这些车轮都会很快解体。

为了解决这个问题， [[Audrey]创造了 OpenWheel](https://hackaday.io/project/16024-openwheel-parametric-osh-wheelstyrestracks) ，这是一个参数化的 3D 打印车轮、tweels、轮胎和机器人轨道等系统。

像所有好的参数化 3D 打印设计一样，OpenWheel 是用 OpenSCAD 编写的。这些不是 3D 设计；它们是编译成可打印对象的代码，用变量来设置半径、厚度、轴的直径、螺栓图案和其他任何形成车轮形状的东西。

包括在这个工具集是一堆轮子和齿轮，可以组装成一个传动系统。到目前为止，可以用柔性细丝打印出某种东西的 3D 可打印轨道几乎还是未知的:完全可配置的 3D 可打印坦克履带。我们现在需要的只是一个 3D 打印的坦克变速器，我们最终将拥有一个完整的 hobby robotics 底盘。