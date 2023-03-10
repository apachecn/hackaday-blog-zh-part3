# 小于 1 KB 的十进制时钟

> 原文：<https://hackaday.com/2016/12/02/decimal-time-clocks-in-under-1-kb/>

人类历史上一直很好地使用十进制计数系统。这可能是因为我们大多数人都有十个手指，这使得以十为基数计数很容易。然而，人类似乎固执地坚持奇怪的十二/六十进制时间系统。[Danjovic]用一个他称之为 DC-10 的十进制时钟给这个混合体带来了一点理智。他已经为我们的 [1 kB 挑战](https://hackaday.io/contest/18215-the-1kb-challenge)报名了。

DC-10 建立在 [C10 的基础上，C10 是由【KnivD】](https://hackaday.io/project/11131-c10)在 Hackaday.io 上创建的十进制时间显示系统

它是这样工作的:

*   1 年= 365.25 天(这个我们无论如何也改不了)
*   1 天= 100 个间隔(相当于“小时”)
*   1 个间隔= 100 厘(相当于“分钟”)
*   1 厘瓦= 100 个刻度(相当于“秒”)
*   1 滴答= 0.0864 当前秒。

植入显示时间间隔和百分位数，正是你需要知道的一天中的当前时间。他使用了一个 4 MHz 时钟的微芯片 PIC16F628。时间显示在七段发光二极管上。PIC 是用 C 语言编程的，使用的是 Microchip 自己的 IDE 的经典版本:MPLAB 8.92。该代码使用 297 个程序字。由于‘628 使用 14 位指令，这相当于不到 520 字节。非常适合 1 kB 挑战！

如果你心中有一个很酷的项目，还有足够的时间[参加 1 kB 挑战](https://hackaday.io/contest/18215-the-1kb-challenge)！截止日期是 1 月 5 日，所以检查一下，发动你的装配工吧！