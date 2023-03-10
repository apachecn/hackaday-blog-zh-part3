# 带视觉的定制键盘

> 原文：<https://hackaday.com/2018/05/26/a-custom-keypad-with-vision/>

廉价的 USB HID 功能微控制器、在线购买单个机械钥匙的能力和 3D 打印的结合开辟了一个专用输入设备的全新世界。偶尔，它们会采用全键盘的形式，但更多的情况下，它们是带有六个左右按键的小键盘，专用于特定的任务，或者偶尔用于特定的游戏或程序。对我们来说，一个简单而廉价的项目，对任何花大量时间坐在电脑前的人来说都是实实在在的好处，听起来肯定是一个胜利。

[![](img/8e113de4c3ab6f19a94cbab0bf244789.png)](https://hackaday.com/wp-content/uploads/2018/05/minikey_detail.jpg) 但是[r0ckR2]的这个构建将这个概念向前推进了一步。他的键盘不仅仅是一个简单的 3×3 键盘，还包括一个显示每个键当前分配的[小屏幕。这不仅在桌面上看起来很酷(总是很重要)，而且它还允许为每个键分配多个功能。该屏幕使用户能够在不同的键分配页面之间切换，潜在地允许为他们使用的每一个软件使用不同的热键或宏。](https://imgur.com/a/h87sC0J)

外壳和键帽都是完全 3D 打印的。为了保持简单，[r0ckR2]没有费心设计一个完整的外壳，让所有的电子设备都暴露在背面。有些人可能认为它有点乱，但我们很欣赏这样一个事实，即如果您需要修复任何东西，它可以让您轻松地访问内部。底部增加了橡胶支脚，这样在使用时不会滑动，但除此之外，这种情况非常简单。

至于电子设备，[r0ckR2]配备了一个 STM32“蓝色药丸”板，因为这是他手头上的东西。屏幕是 ST7735 1.44 英寸 SPI TFT，按键本身是他从易贝得到的樱桃 MX 红色克隆。总而言之，大部分装备来自他的零件箱，或者只是网上的几块钱。

如果你正在寻找更大的东西，看看这个[华丽的 Arduino 驱动版本](https://hackaday.com/2018/02/15/arduino-keyboard-is-gorgeous-inside-and-out/)，或者[这个更实用的版本](https://hackaday.com/2015/03/29/3d-printed-mechanical-keyboard/)。两者几乎都是 3D 打印的，证明这项技术不仅仅能够制造小船。

[通过 [/r/functionalprint](https://www.reddit.com/r/functionalprint/comments/8g2o34/designed_and_printed_a_mini_keyboard_for_gaming/)