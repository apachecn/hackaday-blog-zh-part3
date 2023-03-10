# 五十年记得你的生日

> 原文：<https://hackaday.com/2018/01/16/remember-your-birthday-for-fifty-years/>

我们的硬币电池挑战比赛已经出现了一些令人惊讶的参赛作品，这些东西是我们从如此微薄的能源中不可能想到的。以【毗瑟奴·梅亚】的作品为例，[一个他声称可以在长达五十年的时间里每年点亮作为生日提醒的装置](https://hackaday.io/project/29327-birthday-alarm-thatll-run-for-50-years)。

它的核心是一个经过修改的 Arduino 纳米克隆，从 CR2450N 中提取了测得的 608 nA。根据电池的规格，他已经计算出 50 年的最大值，CR2032 可能为 29 年，CR2477 可能为 64 年。然而，他指出，这并没有把自放电考虑在内，但你可能在十年左右的时间里买得起新电池。

为其“P”版低功耗处理器精心选择的 Arduino 克隆产品已经移除了串行桥 IC 以实现这一功耗，以及稳压器和一些分立元件。有趣的是，他注意到 ATMega168P 比它的 328 表亲更节省，所以他用的是前者的芯片。为实现最低功耗，设置了一系列内部标志，并选择内部振荡器使用尽可能低的时钟速度。有一个 Intersil ISL1208 低功耗 RTC 芯片安装在一块条形板上，用于提供时间，当然还有一个 LED 用于提供基本的生日提醒。

当 LED 灯为这个大日子点亮时，你总有希望收到另一个硬币电池，这一次为边缘发光的音乐生日贺卡供电。

Coin Cell ChallengeBuild something cool powered
by a coin cell, win prizes![Enter now](https://hackaday.io/contest/28283-coin-cell-challenge)[See all entries](https://hackaday.io/submissions/coin-cell-challenge/list)