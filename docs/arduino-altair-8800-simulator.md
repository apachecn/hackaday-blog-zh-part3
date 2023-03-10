# Arduino Altair 8800 模拟器

> 原文：<https://hackaday.com/2017/02/18/arduino-altair-8800-simulator/>

在易贝四处寻找一台原装的 Altair 8800，你会很快发现它的价格范围是几千美元。如果你是一个收藏家，口袋里有些钱，也许这没什么。但是，如果你想在预算范围内获得 Altair 8800 体验，你可以用 Arduino 为自己打造一个克隆版。[David]友好地[在他的 Arduino 项目中心帖子上分享了构建细节](https://create.arduino.cc/projecthub/david-hansel/arduino-altair-8800-simulator-3594a6)。使用 Arduino Due(或原始速度 25%的 Mega)，克隆可以准确地再现 Altair 的前面板元素的行为。我们在过去报道过一个类似的项目，使用的是 [Arduino Uno。](http://hackaday.com/2015/04/12/altair-8800-front-panel-for-an-8080-emulator/)

虽然建造一台电脑并不复杂，但你需要相当大的耐心，这样你才能焊接所有 36 个发光二极管、开关、晶体管和电阻，但最终，你将拥有一台全新的电脑。1975 年，组装的 Altair 8800 电脑售价 621 美元，未组装的售价 439 美元。来源正确的话，你的克隆会低于 50 美元。还不错。

模拟器附带了一堆软件供你试用，甚至还有像 Kill-the-Bit 和 Pong 这样的游戏。仿真器软件中包含 BASIC 和汇编示例程序，可以轻松加载。

此外，模拟器包括一些额外的功能和 Altair 的内置软件，可通过前面板上的 AUX1/AUX2 开关访问(这些功能和软件在最初的 Altair 上包含但未使用)。从启动不同的游戏到在模拟磁盘驱动器中安装磁盘，这里有太多的功能需要描述。你可以看看[模拟器文档](https://github.com/dhansel/Altair8800/raw/master/Documentation.pdf)了解更多信息。

如果你还不知道，以下是如何玩“杀死钻头”的方法:

 [https://www.youtube.com/embed/prdvkMP3FAA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/prdvkMP3FAA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

