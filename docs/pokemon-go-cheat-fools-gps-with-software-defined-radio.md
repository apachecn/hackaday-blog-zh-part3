# 口袋妖怪 Go 欺骗傻瓜 GPS 与软件定义的无线电

> 原文：<https://hackaday.com/2016/07/19/pokemon-go-cheat-fools-gps-with-software-defined-radio/>

使用 Xcode 来欺骗 Pokemon Go 中的 GPS 位置([就像我们今天早上看到的](https://hackaday.com/2016/07/19/pokemon-go-gps-cheat-if-you-dont-fear-getting-banned/))算不上什么黑客，坦率地说，这甚至不是一个*合法的* GPS 欺骗。毕竟，这不像我们[使用 SDR 欺骗物理 GPS 信号来欺骗 Pokemon Go](https://www.insinuator.net/2016/07/gotta-catch-em-all-worldwide-or-how-to-spoof-gps-to-cheat-at-pokemon-go/) 。

对[斯蒂芬·基斯]来说，这只不过是一次练习。他甚至都没在玩口袋妖怪 Go。为了从他的 300 美元的软件无线电 HackRF One 中挤出可用的 GPS 信号，[Stefan]使用了外部精确时钟。这弥补了 HackRF 内部时钟校准的不足，尽管他指出这个[也可能完全在软件](https://github.com/mossmann/hackrf/pull/232)中修复。

使用 [SatGen](http://www.labsat.co.uk/index.php/en/free-gps-nmea-simulator-software) 和软件定义的 GPS 信号模拟器[附带的转换工具 gps-sdr-sim](https://github.com/osqzss/gps-sdr-sim/tree/master/satgen) ，【Stefan】变成了一个*。KML 出口的谷歌地球路径变成了*。可由 GPS 模拟器回放的 CSV 文件。

 [![google_earth_kml](img/0af77a9f335a9370d8597bcce1e80c51.png "google_earth_kml")](https://hackaday.com/2016/07/19/pokemon-go-cheat-fools-gps-with-software-defined-radio/google_earth_kml/)  [![satgen](img/d13be06e62613306a82f7f785b856697.png "satgen")](https://hackaday.com/2016/07/19/pokemon-go-cheat-fools-gps-with-software-defined-radio/satgen/)  [![u-center](img/8c76e194497939b4e3529778ba525fd2.png "u-center")](https://hackaday.com/2016/07/19/pokemon-go-cheat-fools-gps-with-software-defined-radio/u-center/) 

启动 GPS 传输后，他发现自己的虚拟形象在口袋妖怪世界里快乐地奔跑。仍然需要有人来编写代码，让你自由地导航，并且实际上*抓住所有人*，但是这看起来是可行的，我们很好奇它将如何以及是否会影响游戏。对于 SDR 骗子新手，[Stefan]有一些额外的建议:在你的设备上禁用 A-GPS，在 SDR 上使用信号衰减器(屏蔽盒应该可以)。

一个合法的 GPS 欺骗可能仍然会超出一般玩家想要承担的努力和投资。也就是说，如果做得好，你可能会侥幸逃脱。然而，如果做错了，法律后果[可能会更加严重](http://www.gps.gov/spectrum/jamming/)。但是有多少玩家会真的去尝试这个呢？Niantic 能够可靠地检测 SDR 欺诈者吗？你怎么想呢?请在评论区告诉我们！

感谢[sabas1080]的提示！