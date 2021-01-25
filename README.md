## 教程
下载[Fabric](https://fabricmc.net/) 安装器

打开后点击服务端选项，选择所需版本和安装位置进行安装

安装完毕后会弹窗提示缺少服务器核心文件，选择下载(Download server jar)，下载完毕点击生成启动文件(Generate)

运行``start.bat``文件等待命令窗口运行完毕，打开新生成的文件``eula.txt``

将``eula=false``改成``eula=true``后再次运行``start.bat``

当命令窗口显示``For help, type "help"``后输入``stop``关闭服务器
## 配置
服务器配置文件``server.properties``
[配置文件各项汉化介绍](https://www.bilibili.com/read/cv7149916)

要是不喜欢开服后会额外弹窗，右键``start.bat``用记事本打开
在第一行最后加上 ``nogui``
```
java -jar fabric-server-launch.jar nogui
pause
```
## 地毯模组安装
下载对应版本的[Carpet](https://www.curseforge.com/minecraft/mc-mods/carpet)地毯模组
放进``mods``文件夹

地毯端就安装完成，具体配置参考[B站专栏](https://www.bilibili.com/read/cv8371451)
##

## 相关链接
[Fabric](https://fabricmc.net/use/)用于加载Mods 

[Carpet](https://www.curseforge.com/minecraft/mc-mods/carpet)地毯模组 

[MCDR](https://github.com/Fallen-Breath/MCDReforged)用于加载插件 
