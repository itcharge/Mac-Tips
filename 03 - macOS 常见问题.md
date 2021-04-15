# 1. App 打开出现「已损坏无法打开」

如果您下载的应用软件没有通过 Mac App Store 下载，而是来自第三方网站或者平台，那么打开时可能会提示 `XXX 已损坏，无法打开。您应该将它移到废纸篓` 或者 `打不开 XXX,因为它来自身份不明的开发者` ，从而无法运行该应用软件。

![](http://qncdn.bujige.net/images/20200716181853.jpg)

- 原因：这是因为 Mac 启用了安全机制，默认只信任 Mac App Store 下载的软件以及拥有开发者 ID 签名的软件，但是同时也阻止了非开发者签名的软件。

可尝试进行如下步骤：

## 1.1 macOS Mojave 10.14 及以下系统，打开允许「任何来源」开启

1. 打开「启动台」，选择「终端」软件，输入以下命令：`sudo spctl  --master-disable ` 
2. 然后按回车键，继续输入密码（密码输入时是不可见的），输完之后继续按回车键。
3. 接着打开「系统偏好设置」，选择「安全性与隐私」，选择「通用」，可以看到「任何来源」已经选定。
4. 最后，再重新打开应用程序安装软件重新进行安装。

![](http://qncdn.bujige.net/images/20200716182036.jpg)

## 1.2 macOS Catalina 10.15 系统

1. 打开「启动台」，选择「终端」软件，输入以下命令：`sudo xattr -r -d com.apple.quarantine /Applications/XXX.app`
   - 注意：`/Applications/XXX.app` 换成你的 App 路径（将 App 文件拖入终端即可自动显示路径）。
2. 重启 App。

## 1.3 macOS Catalina 10.15.4 系统

1. 安装 Command Line Tools 工具：打开「启动台」，选择「终端」软件，输入以下命令：`xcode-select --install`

2. 继续在终端输入以下命令：`sudo codesign --force --deep --sign - /Applications/XXX.app`

   - 注意：`/Applications/XXX.app` 换成你的 App 路径（将 App 文件拖入终端即可自动显示路径），以下命令行步骤均要替换。

3. 重启 App。

4. 错误解决：

   如果出现以下错误提示：

   - `/文件位置 : replacing existing signature`
   - `/文件位置 : resource fork,Finder information,or similar detritus not allowed`

   那么，则在「终端」执行：`xattr -cr /Applications/XXX.app` 

   然后再执行步骤 2 的命令：`sudo codesign --force --deep --sign - /Applications/XXX.app`

## 1.4 关闭 SIP

如果还不行，可以尝试关闭 SIP 机制（系统完整性保护）。

这是因为 SIP 机制会限制破解文件的调用，所以要关闭 SIP。

1. 查看 SIP 状态：打开「启动台」，选择「终端」软件，输入以下命令：`csrutil status` 如果显示是 `enabled` 则表示 SIP 为打开状态，如果显示是 `disabled`。
2. 如果显示 `enabled` 则需要关闭 SIP。具体操作如下：
   1. 重启 Mac，按住键盘上 「Command ⌘ + R」 组合键，直到屏幕上出现苹果的标志和进度条，进入 Recovery 模式。
   2. 在屏幕最上方的工具栏找到实用工具（从左向右数第 3 个），打开「终端」，输入以下命令：`csrutil disable`，然后按回车。
   3. 关掉「终端」，重启 Mac。
   4. 重启之后，可以在终端按照步骤 1 查看 SIP 状态。
3. 查看 SIP 为关闭状态之后，打开 App。
4. 建议能够打开 App 之后，再打开 SIP，可以通过步骤 2 并执行打开 SIP 的命令：`csrutil enable`

---

# 2. Mac App Store 下载失败

可尝试下面两种方法：

## 2.1 打开 Debug 菜单，刷新 Mac App Store 的 `.plist` 文件

1. 先彻底关闭退出 App Store 软件，可以点击屏幕左上角的  标志，选择「强制退出」，选中「App Store」软件，点击「强制退出」。
2. 打开「启动台」，选择「终端」软件，输入以下命令：`defaults write com.apple.appstore ShowDebugMenu -bool true`。   
3. 重新启动 App Store，尝试下载。

## 2.2 更改网络代理

1. 先彻底关闭退出 App Store 软件，可以点击屏幕左上角的  标志，选择「强制退出」，选中「App Store」软件，点击「强制退出」。
2. 按照以下路径进行点击：「」->「系统偏好设置」->「网络」->「Wi-Fi 页面」-> 右下角选择「高级」->「代理」。
3. 将「代理」中的「网页代理（HTTP）」和「安全网页代理（HTTPS）」的选项勾选去掉，然后点击「好」。
4. 然后再打开 App Store 就好了。

---

# 3. 无法识别移动硬盘

如果是因为没有正确弹出外置移动硬盘，可以尝试下面的命令，正确移除移动硬盘。

1. 打开「启动台」，选择「终端」软件，输入以下命令：`diskutil list`

   此时，终端会显示你的硬盘列表，如下所示：

   ```
   /dev/disk0 (internal, physical):
      #:                       TYPE NAME                    SIZE       IDENTIFIER
      0:      GUID_partition_scheme                        *251.0 GB   disk0
      1:                        EFI EFI                     209.7 MB   disk0s1
      2:                 Apple_APFS Container disk1         250.8 GB   disk0s2
   
   /dev/disk1 (synthesized):
     .......
   
   /dev/disk2 (external, physical):
      #:                       TYPE NAME                    SIZE       IDENTIFIER
      0:     FDisk_partition_scheme                        *30.8 GB    disk2
      1:               Windows_NTFS                         29.9 GB    disk2s1
   ```

2. 找到出问题的移动硬盘对应项，比如上图是 `/dev/disk2`。

   - **注意：千万小心别看错了，别把系统盘给移除了。**

3. 继续在「终端」执行下面的卸载方法：`diskutil unmountDisk /dev/disk2` ，按回车继续。

4. 继续在「终端」执行下面的弹出方法：`diskutil eject /dev/disk2`，按回车继续。

5. 最后拔下移动硬盘，再重新插入。

---

# 4. USB 连接 iPhone，响个不停。

如果我们使用的手机是 iPhone，通过数据线连接 Mac 的时候，iPhone 会响个不停，充电状态总是自动的连上，然后又断开，然后再连上。

可以通过下面两种方式解决问题：

## 4.1 方式 1：旧系统尝试

1. 打开「启动台」，选择「终端」软件，输入以下命令：`sudo killall -STOP -c usbd`，然后按回车，输入密码，继续按回车。
   - 注意：输入上面命令，可能会关闭手机充电，或者使手机充电变慢。如果需要恢复，则输入以下恢复命令：`sudo killall -CONT -c usbd`

## 4.2 方式 2：新系统尝试

1. 打开「启动台」，选择「终端」软件，输入以下命令：`sudo pkill -9 usbd`，然后按回车，输入密码，继续按回车。

---

# 5. Mac 下显示 / 隐藏文件

同 Windows 一样，macOS 会将重要文件隐藏起来，以防止意外删除这些文件而损坏系统。但是，有时候我们需要显示隐藏文件。则需要使用如下方法。

## 5.1 macOS 10.6~10.8 系统：

1. 打开「启动台」，选择「终端」软件，输入以下命令，显示隐藏文件：`defaults write com.apple.Finder AppleShowAllFiles Yes && killall Finder`
2. 如果需要不显示隐藏文件，则执行下面的命令：`defaults write com.apple.Finder AppleShowAllFiles No && killall Finder`

## 5.2 macOS Mavericks 10.9 及以上系统：

1. 打开「启动台」，选择「终端」软件，输入以下命令，显示隐藏文件：`defaults write com.apple.finder AppleShowAllFiles Yes && killall Finder`
2. 如果需要不显示隐藏文件，则执行下面的命令：`defaults write com.apple.finder AppleShowAllFiles No && killall Finder`

---

# 6. 禁用软件的深色模式 / Dark Mode

macOS Mojave 10.14 引入了系统层面的深色模式。但是开启系统的深色模式之后，不光会影响系统自带的应用程序，还会影响第三方的应用程序。如果第三方应用程序没有很好适配的话，显示效果就会很差，甚至会影响使用（例如 「微云同步助手」）。

![](http://qncdn.bujige.net/images/20200729171657.jpg)

可以看到深色模式下部分内容缺失。我们可以通过终端命令来禁用某一软件的深色模式。具体步骤如下：

1. 打开「访达」，选择「前往」，点击「应用程序」。找到你要禁用的「应用程序.app」，例如「微云同步助手.app」，记住该软件名字。

2. 打开「启动台」，选择「终端」软件，输入以下命令来查看应用程序的 Bundle ID：`osascript -e 'id of app "微云同步助手"'`。

   - 其中 **微云同步助手** 需要替换为上一步你看到的软件名字。

3. 继续在「终端」输入以下命令：defaults write com.tencent.WeiyunResona NSRequiresAquaSystemAppearance -bool Yes`

   - 其中 **com.tencent.WeiyunResona** 需要替换为上一步中显示的应用程序 Bundle ID。

   ![](http://qncdn.bujige.net/images/20200729182844.jpg)

4. 重启应用程序，应该已经成功禁用该程序的深色模式了。

> [附] 常用应用程序禁用深色模式命令：
>
> - 网易云音乐：` defaults write com.netease.163music NSRequiresAquaSystemAppearance -bool YES`
> - QQ：`defaults write com.tencent.qq NSRequiresAquaSystemAppearance -bool YES`
> - iBooks：`defaults write com.apple.iBooksX NSRequiresAquaSystemAppearance -bool YES`
> - XCode：`defaults write com.apple.dt.Xcode NSRequiresAquaSystemAppearance -bool YES`
> - Sourcetree：`defaults write com.torusknot.SourceTreeNotMAS NSRequiresAquaSystemAppearance -bool YES`

# 7. 按空格键无法进行预览问题

可以通过重启「访达（Finder）」解决。

键盘按下 **Command ⌘ + Option ⌥ + Esc** 组合键，选中「访达（Finder）」，然后点击「重新开启（Relaunch）」。

