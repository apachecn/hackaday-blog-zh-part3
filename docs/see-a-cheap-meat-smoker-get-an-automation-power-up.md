# 看到一个廉价的吸烟者得到一个自动化电源

> 原文：<https://hackaday.com/2016/09/24/see-a-cheap-meat-smoker-get-an-automation-power-up/>

【杰森】通过[成功自动化这台熏肉机](http://blog.jhambone.com/index.php/2016/09/22/digitally-controlled-meat-smoker/)学到了很多。这只是[杰森的]吸烟者项目的第一步。他决定先从制造更便宜的木炭装置开始，然后再着眼于制造自己的自动颗粒饲料吸烟器。对于木炭吸烟者来说，所有的一切都是为了控制通向热煤床的气流。

[![automated-meat-smoker-air-valve](img/4d73fa34b19d72db2dc8e8e6a356805c.png)](https://hackaday.com/wp-content/uploads/2016/09/automated-meat-smoker-air-valve.jpg)

Custom mount for servo was actually one of the more challenging things to get just right.

[Jason]首先要确保底部密封，防止气流散失，然后他在炭锅上开了一个洞，接上一段钢管。管子的另一端有一个风扇。在管子里面有一个隔板把风扇和炭锅隔开。此处所示的伺服电机控制该阀门。

管道是空气被引入吸烟者的方式，用风扇和阀门来控制流速。空气越多，温度越高。大块的管道没有被切割，工作正常，但比需要的要长得多；[杰森说]烟斗摸起来非常凉，离吸烟者只有一英尺半远。

随着执行器的到位，他需要一个反馈回路。安装在吸烟者盖子上的热电偶由运行 PID 控制回路的 Arduino 监控。这将预测温度变化，并调整挡板和风扇，以避免超过目标温度。最后一个硬件是肉本身内部的温度探头。随着对吸烟者温度的调节和对肉类内部温度的监控，学习(和烹饪)过程正在顺利进行。

有很多吸烟者自动化项目。有的烟民是[用花盆](http://hackaday.com/2012/09/17/some-technical-improvements-on-alton-browns-hacked-smoker/)自制的电烟盒，有的更专注于[改装的下架机组](http://hackaday.com/2011/02/11/pid-controlled-bradley-smoker-clone/)。在某种程度上，每个 PID 控制的吸烟者都是一样的，但他们在创作过程中最终要解决不同的问题。学习 PID 的最好方法就是把它付诸实践，这样你的努力会得到一份美味的回报。