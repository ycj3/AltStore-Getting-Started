# AltStore-Getting-Started

> [官网英文文档说明](https://faq.altstore.io/getting-started/how-to-install-altstore-macos)  

本文将介绍如何借助Mac，实现在iOS设备上安装App IPA的过程

## 必备：
* Mac（本教程MacOS 12.6.3 ）
* iPhone（本教程iPhone 7 plus , iOS 15.7.3 ）
* Apple ID 和 密码
## 步骤：
### Step 1. 通过Mac设备，将AltStore安装到你的iPhone上
1. 下载 [AltServer for Mac](https://cdn.altstore.io/file/altstore/altserver.zip)，双击解压
2. 复制 AltServer.app 到 应用程序
3. 启动 AltServer ，你将在顶部菜单栏中看到它的图标
4. 将iPhone连接Mac（确保设备已解，且已信任Mac）
5. 启用 接入Wi-Fi时显示此iPhone

<img width="610" alt="image" src="https://github.com/CarlsonYuan/AltStore-Getting-Started/assets/123744402/db4d1969-4571-4a63-a9c8-bdf92a5672e3">

6. 点击 AltServer，安装AltStore到iPhone

  ![image](https://github.com/CarlsonYuan/AltStore-Getting-Started/assets/123744402/5158eea0-0abe-4b74-b1ca-7cebd9f0678f)

如果你在上图 “Update Mail Plug-in...“ 看到的是“Install Mail Plug-in...”，那么需要先安装Mail插件，跳转兔哥：启用Mac 邮件(Mail ) AltPlugin 插件 完成插件安装

7. 输入你的Apple ID 和 password（Apple ID 的密码），点击 “install”，等待AltStore成功安装到iPhone

![image](https://github.com/CarlsonYuan/AltStore-Getting-Started/assets/123744402/6705fd8b-f18d-4e89-b39d-96c73f178dca)

8. 在iPhone上，打开设置 -> 通用 -> VPN与设备管理。
找到 “开发者 APP”， 点击上一步输入的Apple ID -> “信任 [你的 Apple ID]“ -> 再次点击 “信任”。

![image](https://github.com/CarlsonYuan/AltStore-Getting-Started/assets/123744402/16419cf6-1791-4e7b-8335-745a3ac8ab68)

恭喜你～～～ 你完成了第一大步也是最重要的一步～

### Step 2. 下载App IPA文件并发送到手机
* 下载ipa文件
* 发送ipa文件到手机

### Step 3. 使用AltStore对IPA文件签名
注意：完成签名需要在电脑上打开AltServer

![image](https://github.com/CarlsonYuan/AltStore-Getting-Started/assets/123744402/34153f92-73d0-49cf-9c30-8ad22766017e)

### Step 4. 等待签名完成，恭喜你拥有你期望安装的IPA了

![image](https://github.com/CarlsonYuan/AltStore-Getting-Started/assets/123744402/f974088d-8e94-4174-a61d-53924451c410)

重签（7天后到期）：和上述步骤3、4相似
* 不需要重新导入ipa
* 手机需要连接电脑，且电脑需要打开Mail和AltServer
* 直接在手机上点“Refresh All”，等待完成就可以重签成功
重签过程中，手机上的效果，见下图

<img width="457" alt="image" src="https://github.com/CarlsonYuan/AltStore-Getting-Started/assets/123744402/87ec3370-4508-467f-be37-abd5c4743ad4">

## 常见问题及解决方案
### The name "XXX" contains invalid character
问题原因：由于IPA包的Bundle display name 包含非英文字符。  
解决方式：
* ipa包重命名为zip文件，解压。
* 进入Payload，右键显示包内容
* 修改里面的 info.plist文件 的 CFBundleDisplayName的值为英文（不能为中文），修改后保存文件
Mac命令行修改:
> /usr/libexec/PlistBuddy -c "Set :CFBundleDisplayName 这里输入英文名" Info.plist

### 登录提示：你的应用版本过低，请升级至最新版本后再登录。点击“确认”后将跳转至最新下载页面
解决方案：用最新的ipa尝试看下（亲测V8.0.49 在iOS 15.8.2上有效, V8.0.33会提示上面登录错误）
  
## 写在最后
这就是这篇教程的全部内容，如果对你有帮助，感谢Star～  
本教程，步骤较多～ 如果遇到问题，欢迎提issues或在讨论区交流，感谢🙏
