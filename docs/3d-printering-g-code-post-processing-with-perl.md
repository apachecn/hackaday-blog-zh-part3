# 3D 打印:用 Perl 进行 g 代码后处理

> 原文：<https://hackaday.com/2016/07/20/3d-printering-g-code-post-processing-with-perl/>

如果您现有的 3D 打印工具链还没有学会如何使用五头热塑性塑料喷液头产生像样的结果，我们大多数心爱的工具，如 Slic3r、Cura 或 KISSlicer，都提供了脚本接口，可以提供很大的帮助。使用脚本，有可能调整一点点来获得很好的结果，插入擦塔或主塔和清除移动，如果你的设置需要它，还可以控制火焰喷射器的额外伺服和螺线管。

本文简要介绍了如何使用 Perl 和 Slic3r 对 g 代码进行[后处理。Perl 忍者技能不是必需的。Slic3r 可以很好地与几乎所有生成可执行文件的脚本语言兼容，所以如果您不愿意使用 Perl，您可能能够用您最喜欢的语言复制大多数步骤。](http://manual.slic3r.org/advanced/post-processing)

[![slic3r_wipe_prime](img/ae8f114904449104dd9b07c068489e60.png)](https://hackaday.com/wp-content/uploads/2016/07/slic3r_wipe_prime.png)

A little wipe and prime tower for every extruder, generated with Slic3r and a Perl script.

## 入门指南

您所需要的就是在您的系统上安装 [Slic3r](http://slic3r.org/) 和 Perl。OSX 和 Linux 用户已经有了 Perl，而 Windows 用户需要安装一个 Perl 包，例如[草莓 Perl](http://strawberryperl.com/) 。OSX 用户可以从 Slic3r 的 GitHub 库下载[示例后处理脚本](https://github.com/alexrj/Slic3r/tree/master/utils/post-processing)，它只随 Windows 和 Linux 二进制文件一起提供。

## 主循环

设置完成后，在用户目录中创建一个空的文本文件“postprocessor.pl ”,启动您最喜欢的编辑器，用下面的基本结构填充它:

```
#!/usr/bin/perl -i
use strict;
use warnings;

# the main loop
while (<>) {
  print; # implicitly print an unmodified G-code line back into the file
}

```

第一行阐明了脚本语言，`strict`禁用了一些高级的 Perl 魔法，`warnings`在你做错事的时候对你大喊大叫。菱形操作符`<>`让`while`循环逐行迭代输入文件(我们的 g 代码)。在这个例子中，我们只是打印出 g 代码行中没有改变的内容。
Perl 使用了一个*默认变量* `$_`，在某些地方是隐式使用的。因此，在 Perl 中，以下三个片段的意思(几乎)相同:

```
while (<>){
  print;
}
```

```
while (<>){
  print $_;
}
```

```
while (my $_ = <>){
  print $_;
}
```

Windows 用户可能需要在`while(<>)`循环之前添加`$^I = '.bak';`来创建临时工作副本。

## 从 Slic3r 运行脚本

Slic3r 在模型切片后为您运行后处理脚本。你需要做的就是确保脚本是可执行的(`chmod 755 postprocessor.pl`)，并在 Slic3r 的输出选项中指定脚本的绝对路径。

[![](img/b2cd80d9809d17ed66146a095663cc0a.png)](https://hackaday.com/wp-content/uploads/2016/07/slic3r_perl_path1.png)

## 排除故障

除了使用 Slic3r，您还可以手动将脚本应用到终端中现有的 g 代码文件:

`perl path/to/postprocessor.pl path/to/some.gcode`

这样，您还会得到调试脚本的所有警告和错误。

## 示例脚本:灯丝计数器

上面的脚本还没有修改 g 代码，所以让我们写一个实际做一些事情的脚本。以下脚本跟踪打印过程中的灯丝消耗，并使用 [`M117`](http://reprap.org/wiki/G-code#M117:_Display_Message) 命令将其显示到打印机的 LCD(如果有)上。它只是使用[正则表达式](http://regexone.com/)过滤`E`(挤压机)和`Z` (Z 轴)地址的所有 [`G1/G2`](http://reprap.org/wiki/G-code#G0_.26_G1:_Move) 命令。为了保持此示例的简单性，它仅适用于相对挤出移动:

```
#!/usr/bin/perl -i
use strict;
use warnings;
use Math::Round;

my $consumedFilament=0;

while (<>){
  # a regular expression for the G0/G1 commmand (click it to see what it does)
  if(/^G[01](\h+X(-?\d*\.?\d+))?(\h+Y(-?\d*\.?\d+))?(\h+Z(-?\d*\.?\d+))?(\h+E(-?\d*\.?\d+))?(\h+F(\d*\.?\d+))?(\h*;\h*([\h\w_-]*)\h*)?/){
    # the match variables, just readable
    my $X=$2, my $Y=$4, my $Z=$6, my $E=$8, my $F=$10, my $verbose=$12;
    if($E){
      # tracking how much filament we're using
      $consumedFilament+=$E;
    }if($Z){
      # print the consumed filament to the LCD
      print "\nM117 ".round($consumedFilament)."mm\n";
    }
 }
 print;
}

```

## 擦除/灌注塔脚本

此时，您基本上可以跟踪任何 g 代码命令，也可以插入任意新的 g 代码，例如 [`G1`](http://reprap.org/wiki/G-code#G0_.26_G1:_Move) 打印移动(用于擦塔)或 [`M280`](http://reprap.org/wiki/G-code#M280:_Set_servo_position) 命令来控制伺服。然而，同样清楚的是，通过这种方式，您将花费大量时间编写代码来跟踪 g 代码移动并理解它们。我用上面的方法写了一些后处理脚本，所以如果你需要 wipe/prime towers，[你可以在 GitHub](https://github.com/makertum/Multi-Extrusion-post-processing-scripts-for-Slic3r) 上查看。擦拭/灌注塔是一种很好的方法，可以在多色印刷中的工具更换时将喷嘴从渗出的细丝中释放出来，或者在空闲阶段后开始印刷之前灌注挤出机。当使用颜色切换喷嘴时，后者尤其必要，其中需要从喷嘴中清除先前的颜色。它们也是一个很好的例子，说明 Perl 后处理脚本可以做些什么。

 [![Zero-ooze results](img/ba00c694a890e27c3ad500549ce89645.png "_MG_0158")](https://hackaday.com/2016/07/20/3d-printering-g-code-post-processing-with-perl/_mg_0158/) Zero-ooze results [![slic3r_wipe_prime2](img/ac2e10fd839d7c7373f0eb8f85fb7f90.png "slic3r_wipe_prime2")](https://hackaday.com/2016/07/20/3d-printering-g-code-post-processing-with-perl/slic3r_wipe_prime2/)  [![The nozzle during the wiping move.](img/54c55d292d2d57203a2df8726220a918.png "slic3r_wiping")](https://hackaday.com/2016/07/20/3d-printering-g-code-post-processing-with-perl/slic3r_wiping/) The nozzle during the wiping move.

## 通用模板

由于我们需要在做任何更复杂的事情之前解析大量的 g 代码，我得出的结论是，最好的方法是使用一个模板，使最常见的 g 代码作为子例程可用。例如，最好有一个子程序`process_printing_move()`，在其中你可以指定你想要如何处理 g 代码文件中的每一个印刷动作。你可以[在 GitHub](https://github.com/makertum/Slic3r-Post-Processor-Template) 上下载我的模板，它可以让开发新的单文件后处理脚本变得更容易。下面的例子实现了本文第一个例子中的灯丝计数器，只是可读性更强:

### 模板示例:灯丝计数器

```
my $consumedFilament=0;
sub process_printing_move
{
  # these arguments (XYZE and F) are passed to the subroutine
  my $thisLine=$_[0], my $X = $_[1], my $Y = $_[2], my $Z = $_[3], my $E = $_[4], my $F = $_[5];

  # tracking filament usage
  if($E){
    $consumedFilament+=$E;
  }

  # returning the unchanged line
  return $thisLine;
}

sub process_layer_change
{
  # the available arguments
  my $thisLine = $_[0], my $Z = $_[1], my $F = $_[2];

  # print the consumed filament to the LCD
  my $message="\nM117 ".round($consumedFilament)."mm\n";

  # return modified line
  return $thisLine.$message;
}

```

该模板还缓冲整个 g 代码，并使 Slic3r 的打印参数从关联数组`%parameters`中可供您的代码使用。例如，Slic3r 中指定的灯丝直径通过`$parameters{"filament_diameter"}`变为可用。参数名称与 Slic3r 配置文件中的名称相同。您也可以指定您自己的参数，只需将它们添加到 Slic3r 中的*启动 g 代码*部分作为注释(`; some_parameter = 2`)。对于我们的细丝计数器，这意味着我们也可以计算消耗材料的体积:

```
sub process_layer_change
{
  # the available arguments
  my $thisLine = $_[0], my $Z = $_[1], my $F = $_[2];

  # calculating the volume
  my $volume=$consumedFilament*$parameters{"filament_diameter"}**2*PI/4000;

  # printing the volume to the LCD
  my $message="\nM117 ".round($volume)."cm^2\n";
  return $thisLine.$message;
}

```

## 其他实验应用

我希望您喜欢这篇关于 Perl 和 g 代码后处理的简短介绍。最终，你可以用 g 代码后处理器做更多的事情。一个更有趣的应用是互锁非平面印刷。这个想法是使用互锁的非平面层将层拉应力(FDM 的大弱点)转化为层剪切和压缩应力(FDM 的强项)。由于本地电机似乎在寻找一种产生更强零件的方法，我通过我不久前编写的 g 代码后处理器(不过是用 Java 编写的)运行了他们的 Strati 模型，该处理器沿着正弦波场移动各层。由于移位的层不相交，这仍然可以在常规的 3 轴打印机上打印。

 [![Bildschirmfoto-2015-11-11-um-22.11.09-2](img/5bfc40c1ac280d9c31fbdedcee811ba6.png "Bildschirmfoto-2015-11-11-um-22.11.09-2")](https://hackaday.com/2016/07/20/3d-printering-g-code-post-processing-with-perl/bildschirmfoto-2015-11-11-um-22-11-09-2/)  [![Bildschirmfoto-2015-11-11-um-22.12.39-2](img/8b1d7b55f18d13d6ca9ef1c673d3e2e6.png "Bildschirmfoto-2015-11-11-um-22.12.39-2")](https://hackaday.com/2016/07/20/3d-printering-g-code-post-processing-with-perl/bildschirmfoto-2015-11-11-um-22-12-39-2/)  [![post_processing_wave_field](img/496d8f9b8d0cf0c396aa1e42da6d1fde.png "post_processing_wave_field")](https://hackaday.com/2016/07/20/3d-printering-g-code-post-processing-with-perl/post_processing_wave_field/)