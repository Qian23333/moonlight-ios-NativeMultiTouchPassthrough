# 安装 Installation
### 已为Github用户开测试组， 可通过testflight安装：
### Just opened a testing group for github users：
### https://testflight.apple.com/join/1JDEKywe
### 以后大概不会经常发布ipa文件了。 Guess I'm not going to release ipa files frequently..
### 如果觉得这个fork好用， 请记得点星。
### Give it a star if you find this version helpful.
<br>


# Moonlight-ZWM

# 概述 Overview

Developed for: game play, general remote desktop application.
This fork has developed with `too many deviations` from the original version (go to the release page for details).  It's almost impossible, and I'm not interested in merging the modifications into the official repository.

 <br>

# 注意事项 Notice
### 发布基于本Fork的修改版本，请务必申明来源。偷摸合并代码、功能性抄袭将受本人鄙视。 <br>
### Please acknowledge the source when releasing modified versions based on this fork. Silent code merging and functional plagiarism will be met with disdain.<br><br>
功能说明清单，请前往Release页面查看, 本页面不再更新。目前的代码提交在`noWaterMark`分支。<br>
Feature list on this page will not be updated anymore, please check the release page for details <br>
For latest coding commits go to branch `noWaterMark`.
 <br> <br>

# 添加键盘命令 Add Keyboard Command
![image](https://github.com/user-attachments/assets/0ea0f91c-574d-4408-9c92-d5a3e229807a)
<br>Read this instruction:
[How.to.add.keyboard.command.for.moonlight-iOS](https://b23.tv/fgdRJk8)

<br><br>
# 开发者B站号. Developer on Bilibili

如果你有在用Bilibili， 请关注`True砖家`，了解该fork的最新消息。 <br>
If you are on Bilibili, subscribe `True砖家` to get the latest news of this fork: <br>
https://b23.tv/A0F9v7n


 <br> <br>

# 特别感谢 Special Thanks to:
https://github.com/King0fSpace/moonlight-ios-CustomOSC
<br>On screen control customization of my version originated form this repo (with much more improvements)


# 特别纪念 Special Note
## 为防范抄袭狗Up主 "阿西西的日常" , 该仓库曾在 2024年7月期间暂停公开提交代码。<br>
## To prevent plagiarism by copycat "阿西西的日常 (Axixi's Daily Life)", this repository temporarily suspended public code commits during July 2024.

【阿西西: 我撒谎、偷窃、白嫖，但我是大佬Up主】 
【 Axixi: I lie, I steal, I cheat, but I'm a big shot uploader 】
https://b23.tv/9noIx3i

【"阿西西的日常" : 游戏串流界小偷、假大佬、毒瘤up主】 
【 "Axixi's Daily Life": A thief in the game streaming community, a pretender, and a toxic uploader】 
https://b23.tv/Z0ChSiD<br>
 <br> <br>

# 视频介绍, A Video illutration in Chinese:<br>
https://www.bilibili.com/video/BV1M1421C7FD
  <br> <br>

# Fork缘由

这是首个公开的 iOS 多点触控透传fork。

原版本基于 moonlight-ios 9.0.0 ，2024.2.4 提交的 moonlight-common-c 子模块。 已于2024.04.30合并官方仓库9.0.2的代码修改， 并更新moonlight-common-c。 

2023年12月，原神PC版的隐藏触屏UI被热心网友发现。 我作为一个从ipad mini系列开始入坑原神、PC上操作不来键鼠，更不会用手柄的资深搓屏玩家， 开始对ipad上用触屏UI直接操作原神充满期待。
于是我在 某三流Up主 的QQ群里承担了大部分iOS版的测试，在2024年元旦前，终于有了第一个差不多通用的多点触控iOS版本。但这个版本并不完善， 多点触控经常性的卡死对游戏体验影响非常大。

由于该 三流Up主 作为手柄玩家和非专业iOS开发者对iOS moonlight多点触控串流并上不心，2024年4月本人不得不亲自下场，找到bug根本原因并提交解决代码, 使之第一次可以正常使用多点触控。
<br>
<br>

# 主要特性 Feature List 20240526

- ### 无BUG、健壮的多点触控透传.
  ### Robust, BUG-FREE 10-finger Native Touch Pass-Through.
   经过持续的优化， 多点触透传机制已经非常可靠。
   <br>After subsequent optimizations, the multi-touch pass-through mechanism has become very reliable.<br>
![testt5](https://github.com/TrueZhuangJia/moonlight-ios-NativeMultiTouchPassthrough/assets/78474576/46af86e8-ef69-4923-a36b-0a7b54856b22)
   <br><br>

- ### 由本人在moonlight-android上首创、最受欢迎的触点调速(即灵敏度调节)功能已在iOS上实现。
  ### The most welcomed "touch pointer velocity (sensitivity) tweak" feature, which was first implemented on my Moonlight-Android fork, is now available on iOS version. <br>
  ![image](https://github.com/TrueZhuangJia/moonlight-ios-NativeMultiTouchPassthrough/assets/78474576/48d3f5c3-775c-48ed-8fee-41ea4eece12d)
   <br> 触点在屏幕右边生成时， 其移动速度将按设定值缩放， 在剩下的左边屏幕区域则直接透传触点坐标。透传区与调整区的分割位置可调。
   <br> The pointer velocity tweak zone is on the right side of screen with configurable width, while on the rest part of screen, original coordinates of pointer will be passed through to the remote PC.<br>
![testt6](https://github.com/TrueZhuangJia/moonlight-ios-NativeMultiTouchPassthrough/assets/78474576/d40339be-dcad-4866-b8f0-ff3da310cd25)

   <br><br>

- ### 首创唤醒键盘时，抬起串流界面，保证输入区域不被键盘遮挡。
  ### First implemented stream view lifting for local keyboard, prevent remote typing view from being blocked by local keyboard:
  由于iOS悬浮键盘太难用， 只好做了这个功能。<br>
  I did this because iOS floating keyboard sucks.<br>
  ![image](https://github.com/TrueZhuangJia/moonlight-ios-NativeMultiTouchPassthrough/assets/78474576/e1ac15d4-b4ef-4abd-9d25-13159a9ff4d4)
  ![ViewliftExplained - Copy](https://github.com/TrueZhuangJia/moonlight-ios-NativeMultiTouchPassthrough/assets/78474576/54ecd367-3ebb-43a1-95bb-358e3a9ccc54)
  <br> 注意第二张图， 请用手势让软件知道你要在哪里输入文字， 唤醒键盘后串流视图才会抬升到适当的高度，避免文字输入区域被键盘挡住。以下是gif动图示例： <br> Use Gesture to let the software know where the remote input field is, then stream view will be lifted appropriately (not going to be covered by keyboard). Here's a gif example: <br>
  ![testt7](https://github.com/TrueZhuangJia/moonlight-ios-NativeMultiTouchPassthrough/assets/78474576/6230c225-1296-4be0-b64d-8980fce649c3)
   <br><br>


- ### 键盘工具栏可通过菜单开启或关闭。
  ### Configurable local keyboard toolbar:
  ![image](https://github.com/TrueZhuangJia/moonlight-ios-NativeMultiTouchPassthrough/assets/78474576/88a2eca7-dbbc-46c8-a60e-065a7f44b9fa)
   <br><br>


- ### 重构退出会话手势识别，防止意外退出。
  ### Refactored Session Exit Gesture Recognition to Prevent Accidental Exits.
   由于米家游戏UI左边的方向轮靠近屏幕边缘， 原版的退出桌面手势识别非常容易高频操作下触发，你无法想象在深境螺旋里，桌面突然退出的绝望。我不得不自己写了一个识别器替代iOS原生API， 要求从屏幕边缘滑动到一定距离才能触发退出桌面。<br>
   并且滑动距离的触发门槛、以及要求从哪个边缘开始滑动，已加入设置菜单：
   <br> Due to the Mihoyo game UI's directional wheel on the left being close to the screen edge, the original exit gesture recognition was frequently triggered during intense touch operations. You cannot imagine the despair of suddenly exiting from desktop in the Genshin Impact Spiral Abyss. I had to write a recognizer myself to replace the iOS native API, requiring a swipe from the screen edge to a certain distance to trigger the exit to the desktop. The trigger threshold for the swipe distance and which edge to start the swipe from have been added to the settings menu: <br>
![image](https://github.com/TrueZhuangJia/moonlight-ios-NativeMultiTouchPassthrough/assets/78474576/b2fec7b0-c82a-4bca-aec2-0620f5185b2e)
![longSwipeToExit](https://github.com/TrueZhuangJia/moonlight-ios-NativeMultiTouchPassthrough/assets/78474576/a177b3e6-9b28-4274-b1b9-e4011a8caf86)
   <br><br>


- ### 重构键盘切换手势识别，实现可靠本地输入法键盘唤醒、关闭。
  ### Refactored Tap Gesture Recognition for Reliable Local Keyboard Toggle.
   Moonlight-iOS官方版在检测到屏幕上有三个触点时，直接触发本地键盘切换，这种机制将使三触点的拖动完全失效。而如果采用iOS API提供UITapGestureRecognizer, 手势识别成功率将降低，甚至出现连续无法识别的情况。
   为此我重写了一个TapGestureRecognizer, 识别率几乎达到100%且不影响三触点拖动。为避免误触导致键盘意外唤醒， 为触发手势识别所要求的手指数量 增加了设置菜单。推荐手机设为三指触发， 平板设为四指或更多手指触发(用平板操作你的手掌可能会碰到屏幕，形成第三个触点)
   <br>
   The official version of Moonlight-iOS triggers the local keyboard switch when it detects three touch points on the screen, a mechanism that makes three-point dragging completely ineffective. <br> I also tried  UITapGestureRecognizer provided by iOS native API: the success rate of gesture recognition would decrease, and even continuous failures could occur. Therefore, I rewrote a TapGestureRecognizer with a recognition rate of almost 100% that does not affect multi-point dragging.
   To prevent local keyboard from being invoked unexpectedly, I add the required number of fingers for tap recognizer to the setting menu. It is recommended to set 3-finger triggering on phones and 4 or more on tablets (as your palm might touch the screen, forming a third touch point when using a tablet).
   ![image](https://github.com/TrueZhuangJia/moonlight-ios-NativeMultiTouchPassthrough/assets/78474576/6d62fa86-5f89-42e2-8504-456bef04ba4c)
   <br> 这是在平板上将手指数量设置为4的情况：
   <br>Here's a *.gif example of setting "Fingers to Tap" to 4 on my ipad mini6: <br>
   ![testt5](https://github.com/TrueZhuangJia/moonlight-ios-NativeMultiTouchPassthrough/assets/78474576/747854af-d2aa-467c-9c94-eb07bdf52868)
<br>

# 安装 Installation

安装 release 中的 ipa 文件，需要先对文件进行自签名，或者先越狱、安装巨魔商店。 
推荐侧载方案：Sideloadly, Altstore.

To install the ipa file in release, you need to find a way to sideload the app on iOS, or try to jaibreak or install trollstore.
Recommended sideloading: Sideloadly, Altstore.




<br><br><br><br><br>

[![AppVeyor Build Status](https://ci.appveyor.com/api/projects/status/kwv8vpwr457lqn25/branch/master?svg=true)](https://ci.appveyor.com/project/cgutman/moonlight-ios/branch/master)

[Moonlight for iOS/tvOS](https://moonlight-stream.org) is an open source client for [Sunshine](https://github.com/LizardByte/Sunshine) and NVIDIA GameStream. Moonlight for iOS/tvOS allows you to stream your full collection of games and apps from your powerful desktop computer to your iOS device or Apple TV.

Moonlight also has a [PC client](https://github.com/moonlight-stream/moonlight-qt) and [Android client](https://github.com/moonlight-stream/moonlight-android).

Check out [the Moonlight wiki](https://github.com/moonlight-stream/moonlight-docs/wiki) for more detailed project information, setup guide, or troubleshooting steps.

[![Moonlight for iOS and tvOS](https://moonlight-stream.org/images/App_Store_Badge_135x40.svg)](https://apps.apple.com/us/app/moonlight-game-streaming/id1000551566)

## Building
* Install Xcode from the [App Store page](https://apps.apple.com/us/app/xcode/id497799835)
* Run `git clone --recursive https://github.com/moonlight-stream/moonlight-ios.git`
  *  If you've already clone the repo without `--recursive`, run `git submodule update --init --recursive`
* Open Moonlight.xcodeproj in Xcode
* To run on a real device, you will need to locally modify the signing options:
    * Click on "Moonlight" at the top of the left sidebar
    * Click on the "Signing & Capabilities" tab
    * Under "Targets", select "Moonlight" (for iOS/iPadOS) or "Moonlight TV" (for tvOS)
    * In the "Team" dropdown, select your name. If your name doesn't appear, you may need to sign into Xcode with your Apple account.
    * Change the "Bundle Identifier" to something different. You can add your name or some random letters to make it unique.
    * Now you can select your Apple device in the top bar as a target and click the Play button to run.
