# 虚幻4的Android平台搭建
该项目演示了如何在虚幻4实时开发平台搭建Android开发环境。

```
语言:                  C#、C++
机构:                  优立, https://www.euclideon.com/
日期:                  2022-03-15
Android Studio版本:    2021.1.1.22
Unreal Engine版本:     4.27.1
```

## 快速入门指南
### 安装Android Studio
Android Studio安装的前提必须保证安装了jdk1.8版本以上。
1. 打开[Android Studio官网](https://developer.android.google.cn/studio/)，点击DOWNLOAD ANDROID STUDIO下载。

2. 跳转到下载界面，选择同意条款，并点击下载。

3. 等待下载完成之后，双击android-studio-2021.1.1.22-windows.exe运行。

4. 点击Next，跳转到选择组件界面，保持默认选择的内容即可。

5. 点击Next，跳转到安装路径界面，确保安装位置为默认值。

6. 点击Next，跳转到安装界面，点击Install。

7. 安装完成后，点击Next。

8. 确保选中"Start Android Studio"框，然后单击"Finish"退出安装程序。

### 设置Android Studio 
1. 当"Import Android Studio Settings"对话框出现时，选择"Do not import settings"，然后点击"OK"继续。

2. 若弹出以下界面，点击"Cancel"，跳转到数据共享界面。

3. 在数据共享界面您可以自行选择选项，之后跳转到设置向导界面。

4. 点击Next，跳转到安装类型界面，选择Custom。

5. 跳转到JDK的路径选择界面，保持默认选择。

6. 点击Next，跳转到UI界面风格界面，选择您喜欢的风格。

7. 点击Next，跳转到安装SDK界面，保持默认选择和默认安装的路径。

8. 点击Next，跳转内存分配界面，保持默认即可。

9. 点击Next，跳转到验证设置界面。

10. 确认无误后，点击Next，跳转到许可协议界面，对每一项许可都选择接受。

11. 点击Finish，完成组件安装。

12. 在"Welcome to Android Studio"对话框中打开More Actions下拉列表，然后点击SDK Manager。

13. 在 Android SDK 系统设置中，单击 SDK 工具选项卡，选中"Android SDK Command-Line Tools(latest)"复选框。单击Apply以下载并安装此组件。

14. 安装完成后，请务必重新启动您的计算机。

## 设置安卓NDK
1. 打开虚幻引擎4根目录下的Engine/Extras/Android，运行SetupAndroid.bat

2. 系统提示设置成功后按任意键关闭命令提示符，再重启您的计算机以使更改生效。
