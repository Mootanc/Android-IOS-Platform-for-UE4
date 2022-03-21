# 虚幻4的IOS平台搭建<p align="right">[Android开发](README(Android).md)</p>
该项目演示了如何在虚幻4实时开发平台搭建IOS开发环境。

```
机构:                  优立, https://www.euclideon.com/
日期:                  2022-03-15
iTunes版本:            12.12.3.5
Unreal Engine版本:     4.27.1
```

## 快速入门指南
### Ⅰ安装iTunes
1. 打开[iTunes官网](https://www.apple.com.cn/itunes/)，下拉页面，找到Windows版本，点击即可安装。

2. 等待下载完成之后，双击iTunes64Setup.exe运行。

3. 点击下一步，跳转到安装界面，保持默认，点击安装。

4. 安装完成后，同意软件许可协议即可正常运行软件。

### Ⅱ创建虚幻4项目
在虚幻项目浏览器中，创建一个空白游戏项目，目标平台选择Mobile/Tablet，质量级别选择Scalable 3D or 2D，命名为IOSQucikStart，完成创建。加载项目后，可以将编辑器关闭。

### Ⅲ生成签名证书
要在iOS设备上部署和使用UE4项目，您需要来自Apple的特殊证书。在Windows上为IOS开发生成签名证书是由Apple的开发者网站和虚幻引擎提供的虚幻iOS配置向导（iPhonePackager）应用程序共同完成的。
1. 打开虚幻引擎4根目录下的Engine\Binaries\DotNET\IOS，运行IPhonePackager.exe。

2. 由于在打开iPhonePackager.exe时，预配是特定于项目的，因此它会首先要求您找到项目的文件。找到项目文件后，选择并打开目标项目的.uproject后缀文件。

3. 选择New User选项卡，然后单击Create certificate request and a key pair按钮。

4. 单击该按钮时，将打开生成证书请求对话框。在此框中，输入必填信息：您的 Apple ID、电子邮件地址和姓名（或公司名称）。

5. 单击Generate a key pair，然后选择保存.key文件的位置。

6. 单击Generate Certificate Request，然后选择保存.csr文件的位置。完成后，生成证书请求对话框将关闭，返回到iPhonePackager主窗口。

7. 现在，转到[Apple IOS开发者网站](https://idmsa.apple.com/IDMSWebAuth/signin?appIdKey=891bd3417a7776362562d2197f89480a8547b108fd934911bcbea0110d07f757&path=%2Fregister%2Fagree%2F&rv=1)上的iOS证书页面并登录。__注意：您必须是开发人员计划中注册的开发人员或开发人员计划中的组织团队成员__。
9. 转到[此页面](https://developer.apple.com/account/resources/)，点击添加按钮 （+） 以生成新证书。

10. 选择iOS 应用开发，然后点按继续。

11. 单击选择文件，选择之前生成的.csr后缀的证书签名请求文件，然后单击生成，将生成的.cer后缀的证书文件下载到您的计算机。



### Ⅳ添加设备
您必须通过[Apple IOS开发者网站](https://idmsa.apple.com/IDMSWebAuth/signin?appIdKey=891bd3417a7776362562d2197f89480a8547b108fd934911bcbea0110d07f757&path=%2Fregister%2Fagree%2F&rv=1)添加您希望能够在开发过程中安装UE4项目的所有设备。
1. 转到[此页面](https://developer.apple.com/account/resources/)，点击添加按钮 （+） 以添加新设备。

2. 选择"注册设备"，输入设备的名称和 UDID，然后单击继续。查看您输入的信息，然后点击注册。

### Ⅴ创建应用ID
应用 ID 是由两部分组成的字符串，用于标识单个开发团队中的一个或多个应用。
1. 转到[此页面](https://developer.apple.com/account/resources/)，点击添加 （+） 按钮以添加新的应用 ID。

2. 输入应用 ID 的名称，为您的应用程序 ID 选择应用程序 ID 前缀。为要创建和设置捆绑 ID 的应用程序 ID 类型选择通配符。

3. 单击继续，查看信息，然后单击注册。

### Ⅵ创建和导入预配
您必须具有预配配置文件才能将应用安装到 iOS 设备上。预配配置文件包括签名证书、设备和应用 ID。有两种类型的预配配置文件。第一种类型是开发预配配置文件，用于在开发周期内生成和安装应用程序。第二种类型是分发预配配置文件，用于将应用程序提交到 App Store。
1. 转到[此页面](https://developer.apple.com/account/resources/)，点击添加 （+） 按钮以添加新的配置式。

2. 在"开发"下，选择iOS 应用开发，然后单击继续。

3. 选择您之前创建的应用程序 ID，然后单击继续。

4. 选择您之前创建的证书，然后单击继续。

5. 选择要与配置文件关联的所有设备。只有在此处选择的设备才能在其上启动您的应用程序。

6. 输入配置文件的名称，然后单击生成。将生成的.mobileprovision结尾的配置文件下载到您的计算机。

### Ⅶ设置IOS版虚幻编辑器
1. 请确保通过USB数据线将目标iOS设备连接到您的计算机。

2. 打开IOSQuickStart项目。打开Edit->Project Settings窗口。

3. 导航到Platforms->iOS，点击Import Provision，导入预配文件，然后点击Import Certificate，导入证书。

4. 如果已正确设置和导入内容，则应在"状态"中看到"有效"一词。

### Ⅷ在IOS设备上启动项目
1. 单击工具栏中启动按钮旁边的下拉列表，选择您的IOS设备。

2. 当您的关卡在设备上启动时，进度将显示在屏幕的右下角。

3. 部署完成后，在IOS设备上找到该应用程序并将其打开。

### Ⅸ打包IOS项目
1. 选择File->Package Project->iOS。

2. 在目录对话框中，选择要保存的文件的位置。

3. 打包完成后，目标文件夹内将包含一个已准备好部署到 iOS 设备的 IPA。
