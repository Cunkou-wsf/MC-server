## 教程
下载[Fabric](https://fabricmc.net/use/) 安装器

打开后点击服务端选项，选择所需版本和安装位置进行安装``如果要安装MCDR使用插件，先看下面MCDR的安装教程，安装位置选server``

安装完毕后会弹窗提示缺少服务器核心文件，选择下载(Download server jar)，下载完毕点击生成启动文件(Generate)

运行``start.bat``文件等待命令窗口运行完毕，打开新生成的文件``eula.txt``

将``eula=false``改成``eula=true``后再次运行``start.bat``

当命令窗口显示``For help, type "help"``后输入``stop``关闭服务器
## 配置
服务器配置文件``server.properties``参考B站专栏
[Minecraft 服务器server.properties属性文件介绍 (最详细 最全 汉化)](https://www.bilibili.com/read/cv7149916)by[时光丿Time](https://space.bilibili.com/169563643)

要是不喜欢开服后会额外弹窗，右键``start.bat``用记事本打开
在第一行最后加上 ``nogui``
```
java -jar fabric-server-launch.jar nogui
pause
```
## 地毯端地毯模组安装
下载对应版本的[Carpet](https://www.curseforge.com/minecraft/mc-mods/carpet)地毯模组
放进``mods``文件夹

地毯端就安装完成，具体配置参考B站专栏[[Minecraft|Carpet Mod]地毯全功能说明](https://www.bilibili.com/read/cv8371451)by[ForDream丶梦空](https://space.bilibili.com/412669242)

其他模组的安装同上
## MCDR插件服配置
首先电脑需要配置``Python``环境

win10可以直接在微软商店搜索Python下载

也能访问[Python官网](https://www.python.org/)下载 安装时候把勾都点上

配置好Python环境后
下载[MCDR](https://github.com/Fallen-Breath/MCDReforged/releases/tag/v1.2.2)并解压

安装服务器到``server``文件夹，具体步骤看最前面

打开``MCDReforged\mcdreforged\resources``找到``default_config.yml``和``default_permission.yml``分别打开

``default_config.yml``
```

language: en_us 改成language: zh_cn 

#语言设置为中文

start_command: java -Xms1G -Xmx2G -jar minecraft_server.jar nogui

改成

start_command: java -jar fabric-server-launch.jar nogui

#可以从start.bat文件里直接复制

```

``default_permission.yml``按照``- id``将自己的游戏id添加到owner或admin获取高权限

双击运行``MCDReforged.py``文件即可

``plugins``文件夹是放插件的

## 插件
[这里](https://github.com/MCDReforged/PluginCatalogue) 是一个 MCDR 的插件收集仓库

## 相关链接
[Fabric](https://fabricmc.net/use/)用于加载Mods 

[Carpet](https://www.curseforge.com/minecraft/mc-mods/carpet)地毯模组 

[MCDR](https://github.com/Fallen-Breath/MCDReforged/releases/tag/v1.2.2)用于加载插件 
