# 口袋妖怪 Go GPS 作弊(如果你不怕被禁)

> 原文：<https://hackaday.com/2016/07/19/pokemon-go-gps-cheat-if-you-dont-fear-getting-banned/>

Pokemon Go 从其前身 *Ingress* 继承了一定的 GPS 位置欺骗漏洞，但也在欺骗检测方面取得了进展。既然利用游戏的底层机制是赢家游戏的一部分，为什么不把你的智能手机连上 Xcode，看看这次你能不能打败 Niantic？[戴夫·康罗伊]向你展示如何[回放航路点并激活你的口袋妖怪 Go 曲速驱动器](https://www.youtube.com/watch?v=4h5HyONxBgg)。

黑客(因此称为`Monospace`)基于 Android 和 iOS 上的开发者工具包，也是最容易被游戏禁止的方法。在 Android 智能手机上，你需要从 Play store 获得许多 GPS 欺骗应用程序中的一个，反复点击`About phone`以激活开发者设置，并在那里选择该应用程序作为 GPS 欺骗源。正如[Max]在评论中指出的，你可能还需要安装`mock mock locations Xposed module`，这需要一个`rooted`设备。在 iOS 中，你也可以(很可能)通过 Cydia 安装一个恶搞应用，尽管不越狱最简单的方法是[在 Xcode](https://developer.apple.com/library/ios/referencelibrary/GettingStarted/DevelopiOSAppsSwift/Lesson2.html) (或者你手头的任何 iOS 应用)中创建一个新的 iOS 应用，并将其内置到手机中。在调试模式下，您可以加载一个*。GPX 文件，这是一个简单的文本文件，包含基于 XML 的 GPS 交换格式的 GPS 航路点:

```
<gpx>
  <name>My waypoints</name>
  <wpt lat="34.143895" lon="-118.151556">
    <name>SupplyFrame, Inc.</name>
  </wpt>
</gpx>
```

您还可以创建定时路线:

```
<gpx>
 <name>My tracks</name>
  <trk>
    <name>Some track</name>
    <trkseg>
      <trkpt lat="34.143657" lon="-118.152368"><time>2016-07-18T00:00:00Z</time></trkpt>
      <trkpt lat="34.144502" lon="-118.152368"><time>2016-07-18T00:01:00Z</time></trkpt>
      <trkpt lat="34.144490" lon="-118.150470"><time>2016-07-18T00:02:00Z</time></trkpt>
      <trkpt lat="34.143654" lon="-118.150455"><time>2016-07-18T00:03:00Z</time></trkpt>
    </trkseg>
  </trk>
</gpx>
```

通过`Product -> Debug -> Simulate Location -> Add GPX file to project`加载文件，如视频所示。这使得可从`Simulate Location`菜单中选择航路点或轨迹。从那里，你可以*将你的手机传送到指定的位置，或者带着它沿着追踪点散步。*

虽然这个视频更像是一个如何被禁止进入游戏的教程，但如果你尝试了，我们不会在这里评判你。相反，我们更希望看到这样一种实现，即*抓住所有的*而不被 Niantic 设置的各种字符串绊倒，有效地将 GPS 欺骗变成自己的游戏。看看下面的视频，看看[戴夫·康罗伊的]方法。

哦，我们有没有提到这可能会让你被禁赛？怎么强调这一点都不为过。

 [https://www.youtube.com/embed/4h5HyONxBgg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/4h5HyONxBgg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

