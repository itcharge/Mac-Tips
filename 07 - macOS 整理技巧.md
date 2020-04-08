# 1. 程序坞整理技巧

在 macOS 中程序坞（Dock）可用来存放操作系统中任意的程序和文件，而且存放数目不受限制，可以动态更改大小，并在鼠标靠近时自动放大。在默认状态下它位于屏幕底部，但用户可以更改设置将其移到屏幕的左边或者右边。没有被加入 Dock 的程序，在运行的时候，其图标会在 Dock 中被显示出来，并在程序退出之后消失。

Dock 栏主要分为五大部分：程序区、分隔线、堆栈区、最小化窗口和废纸篓。

- 程序区：存放「应用程序」的区域，包括「访达」、「启动台」、「系统偏好设置」等快捷方式和其他应用程序。其中「访达」不可以从程序坞中移除，其他应用程序都可以移除。
- 分隔线：左侧为「程序区」，右侧为「堆栈区」。在分隔线区域点击右键，就可以弹出「程序坞偏好设置」面板，快捷的进行设置了。左键按住不放，还能快速的对「程序坞」进行大小调节。
- 堆栈区：存放「文件」和「文件夹」的区域。除了这两项，还包括「最小化窗口」和「废纸篓」。

![dock-icon](http://qncdn.bujige.net/images/20200401113842.png)

## 1.1 程序坞中添加 / 删除 / 移动应用程序快捷方式

- 添加：打开「启动台」或「应用程序」文件夹，将想要添加的应用程序拖入「程序坞」即可。或者在应用程序打开的情况下，右键点击「程序坞」中该应用程序的图标，选择「选项」，勾选上「在程序坞中保留」。

- 删除：将「程序坞」中的应用程序图标向上拖出「程序坞」，或者将「程序坞」中的图标拖入废纸篓即可。如果为了防止误移除，则可以右键点击「程序坞」中的应用程序，选择「选项」，去除「在程序坞中保留」的勾选。

- 移动：鼠标按住「程序坞」中的应用程序，可以对其进行左右移动。

## 1.2 程序坞基本设置

右键「程序坞」中的分隔线，选择「程序坞偏好设置」。或者桌面左上角点击「菜单栏」的 「 按钮」，选择「系统偏好设置」，再选择「程序坞」，即可打开「程序坞偏好设置」。

![dock-setup](http://qncdn.bujige.net/images/20200401141706.png)

在这里可以对「程序坞」进行一些基本设置。

## 1.3 增加空白占位符

当我们开启的「应用程序」多起来之后，「程序坞」就会显得很杂乱，切换程序的时候，就无法快速的找到自己想要切换的程序。我们可以通过对「程序坞」增加「空白占位符」的方式，为「程序坞」做一下分类。

> 操作步骤：
>
> 打开「应用程序」->「实用工具」->「终端」，输入增加「空白占位符」的命令，点击回车。

- 在「应用区」添加空白占位符的命令：

  ```
  defaults write com.apple.dock persistent-apps -array-add '{"tile-type"="spacer-tile";}'; Killall Dock
  ```

- 在「堆栈区」添加空白占位符的命令：

  ```
  defaults write com.apple.dock persistent-others -array-add '{tile-data={}; tile-type="spacer-tile";}'; Killall Dock
  ```

重复执行上述命令，就可添加多个占位符。最终效果如下：

![dock-dividing-line](http://qncdn.bujige.net/images/20200401143400.png)

## 1.4 隐藏应用使用透明图标显示

通常情况下，如果没有手动勾选「将窗口最小化为应用程序图标」选项，我们在使用 **Command ⌘ + M** 快捷键将应用程序最小化的时候。应用程序会在右侧以缩略窗口展示，十分容易区分。

但是使用 **Command ⌘ + H** 快捷键对应用程序进行隐藏的时候，并没有明显的标识可以识别出隐藏的应用程序，使用下面的命令，可以让那些包含隐藏窗口的应用程序图标变暗。

- 隐藏应用使用透明图标显示的命令：

```
defaults write com.apple.dock showhidden -bool true; Killall Dock
```

- 恢复为默认设置的命令：

```
defaults delete com.apple.Dock showhidden; Killall Dock
```

## 1.5 只显示已打开的应用程序

默认情况下，程序坞会将用户未设置「在程序坞中保留」，却已经打开的应用程序显示出来。时间久了，那些不活跃的「应用程序」一直显示在「程序坞」中，就会令「程序坞」变得杂乱。可以通过下面的命令，可以让「程序坞」只显示已打开应用，以减少不必要的干扰。

- 只显示已打开的应用程序的命令：

```
defaults write com.apple.dock static-only -boolean true; killall Dock
```

- 恢复为默认设置的命令：

```
defaults delete com.apple.dock static-only; killall Dock
```

## 1.6 堆栈高亮效果

默认情况下，将「堆栈区」的「显示内容为」选项设置为「网格」时，当我们鼠标的光标移动经过应用程序图标时，没有高亮效果（其他视图有高亮效果）。通过以下命令，可以启动「网格」视图下的高亮效果。

- 启用堆栈区图标高亮的命令：

```
defaults write com.apple.dock mouse-over-hilite-stack -bool TRUE; killall Dock
```

- 恢复为默认设置的命令：

```
defaults delete com.apple.dock mouse-over-hilite-stack; killall Dock
```



![dock-highlight](http://qncdn.bujige.net/images/20200401145414.png)

# 2. 启动台整理技巧

启动台（Launchpad）可以显示 macOS 中所有安装的软件。随着 Mac 电脑使用时间的增长，我们安装软件的软件也会越来越多。如果长期对启动台缺乏整理的话，启动台就会显得杂乱无章，使用起来极为不便。

如果可以一些方法对启动台进行有效的整理，将会大大提升我们日常使用的便捷度。

## 2.1 更改启动台快捷方式

推荐使用快捷方式来启动「启动台（Launchpad）」。

「桌面左上角菜单栏」 ➡︎「 标志」➡︎「系统偏好设置」➡︎「键盘」➡︎「快捷键」➡︎「启动台与程序坞」

选项卡中有一个「显示启动台」的选项，可以更改启动的快捷方式。

![](http://qncdn.bujige.net/images/20200408112403.png)

## 2.2 更改应用程序显示数目

默认情况下，应用的显示数目为每行 7 个图标，总共有 5 行。



![](http://qncdn.bujige.net/images/20200408140222.png)

我们可以通过命令行的方式对显示效果进行更改。

> 操作步骤：
>
> 打开「应用程序」->「实用工具」->「终端」，输入下面的命令，点击回车。

- 更改每行显示应用程序的个数的命令：

```
defaults write com.apple.dock springboard-columns -int 5
```

- 更改应用程序总共显示的行数的命令：

```
defaults write com.apple.dock springboard-rows -int 3
```

最后，更改完成之后，还需要重启「启动台（Launchpad）」来应用更改。

> **注意：**
>
> **在重新启动「启动台（Launchpad）」之后，所有的应用程序图标排列方式都会被重置，包括文件夹显示，图标排列顺序等等。请慎重操作。**

- 更改设置，重启启动台的命令：

```
defaults write com.apple.dock ResetLaunchPad -bool TRUE; killall Dock
```

![改为 5*3 的效果图](http://qncdn.bujige.net/images/20200408141322.png)



重启之后可以看到，应用全部被重置了，且显示数量发生了更改。

这里我个人设置为 8*4，并且进行了文件夹分类。大家可以按照自己的需求来选择设置图标显示数量效果。

![](../../../WeiYunDrive/Blog%20Images/20200408145539.png)

## 2.3 文件夹分类整理

跟 iOS、iPadOS 上一样，Mac 下的应用程序图标也可以拖进文件夹进行分类显示。

具体操作为：按住某个「应用程序」的图标，将其拖动到其他「应用程序」图标或「应用程序文件夹」上停留，就会显示出文件夹样式，将其放入即可将两个「应用程序」或多个「应用程序」放到一个「文件夹」中。

![](http://qncdn.bujige.net/images/20200408145539.png)

## 2.4 利用第三方软件整理

这里介绍一款软件，「[Launchpad Manager](http://launchpadmanager.com/)」。这是一款帮你快速整理启动台的工具。

Launchpad Manager 可以方便的帮助你对「应用程序」进行按字母序列排序，移动，分组，删除（仅删除图标，不删除应用），创建新的分页等等。

![](http://qncdn.bujige.net/images/20200408153901.png)

> 注意：
>
> **Regenerate 按钮会将所有图标重置为默认效果，请谨慎操作。**

# 3. 菜单栏整理技巧

在 macOS 中，「菜单栏」分为「苹果菜单」、「应用菜单」和「图标栏」。使用时间久了，就会造成应用图标堆积，就像下图这样。

![image-20200408154607399](http://qncdn.bujige.net/images/20200408154608.png)

这样十分不方便我们快速启动自己想要的软件。我们就需要对其进行适当的整理。这里主要是依靠第三方软件来进行整理。

推荐 3 个软件：[Bartender](https://www.macbartender.com/)（付费）、[Dozer](https://github.com/Mortennn/Dozer)（免费）、[Vanilla](https://matthewpalmer.net/vanilla/)（免费）。

其中最好用的是 [Bartender](https://www.macbartender.com/)（付费）。其他两者差不多，选择其中一个即可。

下面讲解一下 Bartender 的使用方法。

![Bartender 的设置界面](http://qncdn.bujige.net/images/20200408163933.png)

Bartender 将图标分为了四级：显示、隐藏、总是显示、总是隐藏。

- 显示和总是显示：不对图标进行操作，直接显示在菜单栏。
- 隐藏：将图标隐藏到创建的二级菜单中，通过点击菜单栏的 Bartender 对应的图标进行显示。
- 总是隐藏：将图标完全隐藏起来，菜单栏和二级菜单中都看不到图标。

通过对不同应用程序图标的设置，经过整理后可以达到以下效果。

![](http://qncdn.bujige.net/images/20200408162645.png)

# 参考链接

- [1] [装点你的 Dock：外观篇丨一日一技 · Mac](https://sspai.com/post/33493)
- [2] [Mac Launchpadの整理と活用方法](https://do-zan.com/mac-launchpad/)

