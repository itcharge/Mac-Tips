# 前言

这篇文章写给刚开始使用 Mac 的小白。

如果你刚刚买了一台 Mac 电脑，却发现用起来不是很顺手；或者你工作、生活使用的是 Windows 电脑，偶尔接触到 Mac 电脑，却不知道怎么使用，我希望通过这篇文章，让你对 Mac 电脑有一个大致的了解。

另外，接受新事物总需要有个磨合的过程。请抱着第一次接触电脑一样的心态去学习使用 macOS 吧。等你适应之后，它将会成为你工作、生活、娱乐上的好伴侣。

---

# 1. Mac & macOS

我们经常提到 Mac 电脑，到底 Mac 电脑指的是什么电脑？而 macOS 又是什么呢？

- **Mac**：通常指的就是是苹果电脑。苹果公司把自己生产的一系列电脑统称为 Mac。包括苹果公司生产的 Mac 笔记本电脑、Mac 一体机，Mac 主机，统称为 **「Mac 」**。
  - **Mac 笔记本**：包括 MacBook（停售）、MacBook Air（在售）、MacBook Pro（在售）。
  - **Mac 一体机**：名字叫 iMac，性能更好的一体机叫 iMac Pro。
  - **Mac 主机**：产品有两个，一个是 Mac Pro（性能最强）、另一个是 Mac mini（主打便携）。

![](http://qncdn.bujige.net/images/20200325153748.png)

- **macOS**：类似于大部分电脑中安装的 Windows 系统、手机上运行的 Android、iOS 系统，Mac 电脑运行的系统就叫做 macOS。在购买 Mac 电脑的时候，macOS 是直接预装在 Mac 电脑上的，不需要用户在额外安装系统。


---

# 2. macOS 和 Windows 的不同

## 2.1 软件并不通用

Windows 系统下的软件后缀名通常为`.exe`，而 macOS 系统下的软件后缀名为`.app`。只有软件厂商专门为 macOS 编写相应的软件才能在 macOS 上运行（通常为某某软件 Mac 版 / 某某软件 for Mac 版）。当然，很多软件会同时提供 Windows 和 macOS 版，我们直接下载对应的 macOS 版本就好了。

![](http://qncdn.bujige.net/images/20200325161045.png)

## 2.2 文件结构不同

macOS 的文件系统格式是 APFS，而 Windows 的文件系统格式是 NTFS。因为版权和商业上的原因，macOS 名义上只能读取 NTFS 格式的硬盘，不支持写入。但是我们可以使用第三方付费软件（例如 [Paragon NTFS](https://china.paragon-software.com/home-mac/ntfs-for-mac/)、[Tuxera NTFS](https://www.tuxera.com/products/tuxera-ntfs-for-mac-cn/)）来读写 NTFS 格式的硬盘，或者将移动硬盘改为兼容格式（ExFAT）。

macOS 中的硬盘也可以分区，但是不像 Windows 一样有「C 盘、D 盘、E 盘、F 盘」这种「盘符」的概念。每个磁盘只有一个名称，没有字母序号。

`Macintosh HD` 就相当于 Windows 的 C 盘。 `Macintosh HD` 盘里分为 **「系统」**、**「资源库」**、**「应用程序」**、**「用户」** 几个文件夹。**「系统」** 相当于 Windows 的 C 盘中的 `WINDOWS` 文件夹，存放的是操作系统文件，不要进行修改。**「资源库」** 里存放这一些系统和软件的配置，不要随意修改。**「应用程序」** 相当于 Windows 中的 `Program Files` 文件夹，应用软件安装在这里边。**「用户」** 相当于 Windows 中 `C:/User/` 文件夹。里边为每一个用户创建了一个用户文件夹（文件夹名为用户名称），每个用户文件夹里包含了 **「下载」**、**「文档」**、**「音乐」**、**「电影」**、**「桌面」**、**「图片」** 等文件夹，这跟 Windows 是一样的。



## 2.3 键盘快捷键不同

Windows 上有四个常用控制键：Shift、Ctrl、Alt、WIN 键。

macOS 上也有四大控制按键 **⇧（shift）**、**⌃（control）**、**⌥（option/alt）**、**⌘（command）**。

macOS 上的常用快捷键和 Windows 略有不同，大体上是相似的。

不同点比如 Windows 上复制、粘贴的快捷键是 **Ctrl + C**、**Ctrl + V**。而 macOS 上是 「**⌘ + C**」、「**⌘ + V**」。

## 2.4 其他习惯不同

macOS 的桌面、顶部菜单栏、Dock 程序坞、Finder 等都和 Windows 有相似的地方，又有特别的地方。这些我们在接下来的 macOS 使用中来讲解。

---

# 3. macOS 使用

## 3.1 开机设置

- 按下 Mac 电脑的电源键开机（笔记本电脑在键盘的右上角）。

如果是首次开机，就会有一个如下图所示的开机提示。按照提示去完成每一步，每完成一步就点击下一步操作。

![](https://support.apple.com/library/content/dam/edam/applecare/images/zh_CN/macbook/osx-el-capitan-setup-macbook-gold-open.png)

- 根据开机提示，设置 Mac

可以参考一下步骤进行设置，具体以 Mac 上的系统提示为准。

1. 选择地区，选择「中国」，点击「继续」。
2. 选择键盘布局和输入法，选择「简体中文」，勾选「简体拼音」，点击「继续」。
3. 选择连接 Wi-Fi，选择家里的 Wi-Fi，然后填写密码，点击「继续」。
4. 选择语言，选择「简体中文」，点击「继续」。
5. 迁移助理，这一步是为之前使用过 Mac 的人准备的，没有用过 Mac 的可以直接点击「继续」。
6. 有 TouchBar 的这一步要设置触控 ID，把手放到 TouchBar 右上角提示位置，重复多次，直到生成完整的指纹。
7. 开启你的位置信息，建议「开启」。
8. 提示使用 Apple ID 登陆的信息。使用 Apple ID 登陆可以访问所有 Apple 服务并使所有设备实现无缝协作。强烈推荐使用 Apple ID 登陆，当然也可以选择稍后登陆。
   - 关于如何创建 Apple ID，可以参考这篇官方教程：[在您的电脑上创建 Apple ID](https://support.apple.com/zh-cn/HT204316#macos)
9. 服务条款，点击「同意」。
10. 设置 iCloud，iCloud 用于 Apple 各种服务的同步，例如照片、联系人、Safari 书签等等，建议「开启」。



## 3.2 macoS 桌面

当我们登录之后，就进入了 macOS 的「桌面」，「桌面」是 macoS 的主屏幕区域。用来放置一些软件，文件，文件夹等。macOS 下的桌面和 Windows 系统的桌面有很多相似的地方，又有一些不同。

像 Windows 上的「菜单栏」、「任务栏」、「工具栏」，在 macOS 下也能找到对应的内容。Windows 桌面的底部有一个固定的任务栏，而 macOS 则是在顶部有一个固定的「菜单栏」，以及底部的「Dock 栏」。

![](http://qncdn.bujige.net/images/20200326111430.png)

下面，我们先来讲解一下 macOS 的桌面都有什么东西。

### 3.2.1 苹果菜单

- 位置在桌面左上角，那个  图标。对应着 Windows 的开始菜单。
- 包含了 macOS 的常用操作选项。包括：开机、关机、系统偏好设置、强制退出等。

![AppleMenu](http://qncdn.bujige.net/images/20200326135807.jpg)

您可以在这里对电脑进行关机、重新启动。同时也在这里可以打开「系统偏好设置」，来设置系统外观，屏保程序，电脑桌面，鼠标设置、触摸板设置等等，这里有点类似于 Windows 的控制面板。

![ApplePreferences](http://qncdn.bujige.net/images/20201117133944.png)

### 3.2.2 应用菜单

- 位置在  按钮的右侧。包含了当前应用的菜单栏选项。
- 默认显示的是「访达」的菜单栏选项，切换不同的软件会显示其对应的菜单栏选项。
- 例如打开 Word 软件，显示的就是 Word 软件的菜单栏，打开 QQ 软件，显示的就是 QQ 的菜单栏。

![AppleApplicationMenu](http://qncdn.bujige.net/images/20201112151113.png)

### 3.2.3 图标栏

- 位置在桌面右上角。类似于 Windows 右下角的工具栏。

- 默认放置了一些系统常用快捷工具。比如：「Wi-Fi」、「调节音量」、「查看日期和时间」、「输入法状态」、「聚焦搜索」、「Siri」，以及最右侧的「通知中心」。

![AppleToolbar](http://qncdn.bujige.net/images/20200326140212.png)

### 3.2.4 通知中心

- 位置在桌面右上角。点击会弹出通知的侧边栏。风格类似于 iPhone 的通知中心。
- 应用程序 的通知和快捷功能都在通知中心。这里可以显示今天的日期、天气、提醒事项等。还可以快速开关「夜览」、「勿扰模式」。

![AppleNotificationCenter](http://qncdn.bujige.net/images/20200326152519.jpg)



### 3.2.5 程序坞

- 位置在桌面的底部中间。对应 Windows 的底部菜单和状态栏。
- 程序坞上的图标对应是软件的快捷打开方式，全部的图标在「应用程序」或「启动台」里。
- 最左边的笑脸文件夹是「访达」，类似于 Windows 中的「资源管理器」或者说「我的电脑」。
- 最右边的垃圾桶样式的图标是「废纸篓」，类似于 Windows 中的「回收站」，用于回收或清除一些删除的文件。

![](http://qncdn.bujige.net/images/20201117093113.png)

### 3.2.6 启动台

- 点击「程序坞」或者使用「触摸板」进行「四指缩放」操作，就可以显示 macOS 「启动台」，风格类似于 iPhone 的界面。这里放着这台 Mac 电脑上所有安装的软件。
- 我们还可以对电脑软件进行整理，归纳到不同的「分类文件夹」中，甚至如果图标多的话，还可以进行分页。

![AppleLaunchpad](http://qncdn.bujige.net/images/20200326143759.png)



## 3.3 软件相关

### 3.3.1 软件简介

Mac 预先安装了很多「应用程序」，使用软件可以点按「程序坞」中的软件图标，或者点按程序坞中的「启动台」，然后使用「启动台」来打开「应用程序」。

- 系统自带常用 App 列表

| 图标                                                         | 应用程序      | 描述                                                         |
| ------------------------------------------------------------ | ------------- | ------------------------------------------------------------ |
| ![“App Store”图标](http://qncdn.bujige.net/images/20201117143201.png) | App Store     | 查找、购买、安装和更新适用于 Mac 的应用程序，请参阅[《App Store 使用手册》](https://support.apple.com/zh-cn/guide/app-store)。 |
| ![“计算器”图标](http://qncdn.bujige.net/images/20201117143216.png) | 计算器        | 执行基本计算、高级计算或编程器计算。请参阅[《计算器使用手册》](https://support.apple.com/zh-cn/guide/calculator)。 |
| ![“日历”图标](http://qncdn.bujige.net/images/20201117143230.png) | 日历          | 日历软件，制定并跟踪会议、日程和约会。请参阅[《日历使用手册》](https://support.apple.com/zh-cn/guide/calendar)。 |
| ![“提醒事项”图标](http://qncdn.bujige.net/images/20201117143248.png) | 提醒事项      | 为待办事项、项目、购物和其他任何需要跟踪的事项创建列表。请参阅[《提醒事项使用手册》](https://support.apple.com/zh-cn/guide/reminders)。 |
| ![“Keynote 讲演”图标](http://qncdn.bujige.net/images/20201117143301.png) | Keynote 讲演  | 类似于 PPT，使用图像、媒体、图表、动画等创建演示文稿。请参阅[《Keynote 讲演使用手册》](https://support.apple.com/zh-cn/guide/keynote)。 |
| ![“Numbers 表格”图标](http://qncdn.bujige.net/images/20201117143311.png) | Numbers 表格  | 类似于 Excel，使用公式、函数、交互式图表等创建电子表格。请参阅[《Numbers 表格使用手册》](https://support.apple.com/zh-cn/guide/numbers)。 |
| ![“Pages 文稿”图标](http://qncdn.bujige.net/images/20201117143330.png) | Pages 文稿    | 类似于 Word，使用格式化的文本、图像、媒体、表格等创建文稿。请参阅[《Pages 文稿使用手册》](https://support.apple.com/zh-cn/guide/pages)。 |
| ![“预览”图标](http://qncdn.bujige.net/images/20201117143342.png) | 预览          | 查看和编辑 PDF 及图像、导入图像以及拍摄屏幕图片。请参阅[《预览使用手册》](https://support.apple.com/zh-cn/guide/preview)。 |
| ![“Safari 浏览器”图标](http://qncdn.bujige.net/images/20201117143355.png) | Safari 浏览器 | 将备忘录、列表和图片保留在桌面上。请参阅[《Safari 浏览器使用手册》](https://support.apple.com/zh-cn/guide/safari)。 |
| ![备忘录图标](http://qncdn.bujige.net/images/20201117143408.png) | 备忘录        | 通过添加照片、视频、URL 或表格来记下迸发的灵感以供稍后整理。请参阅[《备忘录使用手册》](https://support.apple.com/zh-cn/guide/notes)。 |

我们以「日历」软件为例，简单介绍一下 macOS 里的软件的操作使用。

在「启动台」中打开「日历」软件。可以看到桌面中间多了一个界面，如下图所示，这个就是是「日历」软件的「窗口」。我们在这里可以对软件进行操作使用。

![](http://qncdn.bujige.net/images/20201113114416.png)

在桌面的左上角，苹果标志  右侧，就是「日历」的菜单栏选项。在这里可以对「日历」进行一些设置操作。

![](http://qncdn.bujige.net/images/20201113115523.png)

软件的相关设置，大多都可以在软件的「菜单栏选项」中的「偏好设置」里边进行设置，如下图所示。

![](http://qncdn.bujige.net/images/20201113115813.png)

### 3.3.2 软件下载

macOS 系统下的软件后缀名为`.app`。和 Windows 下的软件并不通用。我们需要下载对应的 macOS 版本软件。

macOS 的软件一般来说有两种常用下载方式：

- App Store：苹果官方提供的 App 商城，在 macOS 系统的「启动台」中或者「应用程序」文件夹中可以找到 App Store 的应用软件。
- 应用官网：如果应用没有在 App Store 上线，可以去应用的官网下载 macOS 版本的软件。

> 注：关于 Mac 有哪些好用的软件，具体可以看我写的这篇文章： [**04 - macOS 软件清单**](https://github.com/bujige/macOS-Tips/blob/master/04%20-%20macOS%20%E8%BD%AF%E4%BB%B6%E6%B8%85%E5%8D%95.md)。

### 3.3.3 软件安装

macOS 版本的软件安装包后缀名通常是`.dmg` 或者是`.pkg`。

- `dmg` 是苹果的压缩镜像文件，类似于 Windows 下的 `ISO`。

  打开里面一般包含 `应用程序名.app` 的图标和一个应用程序文件夹 `/Applications` 的快捷方式。

直接将图标拖曳至应用程序文件夹，即可完成安装。

![](http://qncdn.bujige.net/images/20200325161109.png)

- `pkg` 是 macOS 下软件的安装器，按照提示，一步步点击安装即可。

![](http://qncdn.bujige.net/images/20200325161124.png)

### 3.3.4 软件卸载

Mac 下的软件卸载很简单，打开「访达」，在左侧「个人收藏」中找到「应用程序」文件夹，找到你要卸载的软件，点击右键，选择「移动废纸篓」，就完成卸载了。

![](http://qncdn.bujige.net/images/20200326152102.png)



---

# 结语

看到这里，我相信你会对 Mac 的使用有了基本的了解。知道了 macOS 的使用逻辑，软件的安装、使用，以及一些简单的用法。接下来就需要你多去使用和尝试。

接下来，我会尝试写一些关于使用 Mac 的常见问题，系统技巧，整理技巧，软件清单推荐，效率指南等等一系列的文章。请关注我的后序文章。

# 参考资料

- [macOS 使用手册](https://support.apple.com/zh-cn/guide/mac-help/welcome/mac)

- [Mac 入门指南 2.0](https://zhuanlan.zhihu.com/p/83863239)

