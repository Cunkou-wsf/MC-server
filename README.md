## 教程
下载[Fabric](https://fabricmc.net/use/) 安装器

打开后点击服务端选项，选择所需版本和安装位置进行安装``如果要安装MCDR使用插件，先看下面MCDR的安装教程，安装位置选server``

安装完毕后会弹窗提示缺少服务器核心文件，选择下载(Download server jar)，下载完毕点击生成启动文件(Generate)

从java官网下载zip文件解压放到同一目录，以我自己的java版本为例，``jdk-16.0.1``和``start.bat``文件是在同一个文件夹里的

``start.bat``右键编辑
```
set JAVA_HOME=jdk-16.0.1//按照自己的java版本来，java文件夹是啥名字就填啥
set PATH=%JAVA_HOME%/bin;%JAVA_HOME%/jre/bin
java -jar fabric-server-launch.jar nogui//这一行是启动参数，会改的可以按自己需求改，不懂的默认就行了
```

运行``start.bat``文件等待命令窗口运行完毕，打开新生成的文件``eula.txt``

将``eula=false``改成``eula=true``后再次运行``start.bat``

当命令窗口显示``For help, type "help"``后输入``stop``关闭服务器
## 配置
服务器配置文件``server.properties``参考B站专栏
[Minecraft 服务器server.properties属性文件介绍 (最详细 最全 汉化)](https://www.bilibili.com/read/cv7149916)by[时光丿Time](https://space.bilibili.com/169563643)

要是不喜欢开服后会额外弹窗，右键``start.bat``编辑
在第一行最后加上 ``nogui``
```
java -jar fabric-server-launch.jar nogui
pause
```
## 地毯端地毯模组安装
下载对应版本的[Carpet](https://www.curseforge.com/minecraft/mc-mods/carpet/files)地毯模组
放进``mods``文件夹

地毯端就安装完成，具体配置参考B站专栏[[Minecraft|Carpet Mod]地毯全功能说明](https://www.bilibili.com/read/cv8371451)by[ForDream丶梦空](https://space.bilibili.com/412669242)

其他模组的安装同上
## MCDR插件服配置
首先电脑需要配置``Python``环境

win10可以直接在微软商店搜索Python下载

也可以直接访问[Python官网](https://www.python.org/)下载 安装时候把勾都点上

安装好Python后打开cmd输入python，安装成功会显示对应安装的版本号

下载[MCDR](https://github.com/Fallen-Breath/MCDReforged)推荐下方的指令安装
在CMD中输入``pip install mcdreforged``安装，国内镜像源``pip install mcdreforged -i https://pypi.tuna.tsinghua.edu.cn/simple``

在Python的安装目录中依次打开``\Lib\site-packages``，可以找到``mcdreforged``文件夹，把整个文件夹复制到自己想要的位置

打开``mcdreforged``文件夹，空白处右键``在 windows 终端 中打开``，输入指令``python -m mcdreforged init``

找到新生成的``config.yml``和``permission.yml``

``config.yml``
```

language: en_us 改成language: zh_cn

#语言设置为中文

start_command: java -Xms1G -Xmx2G -jar minecraft_server.jar nogui

改成

start.bat

#要改启动选项可以直接在start.bat文件里改

```

``permission.yml``按照``- id``将自己的游戏id添加到owner或admin获取高权限
如我的游戏id是``wangshifu``,我想要有最高的权限，就在``owner:``后加上``- wangshifu``

之后将已有的服务器文件放到``server``文件夹里

再次双击运行``__main__.py``文件即可启动服务器

``plugins``文件夹是放插件的

## 插件
[这里](https://github.com/MCDReforged/PluginCatalogue/blob/catalogue/readme-zh_cn.md) 是一个 MCDR 的插件收集仓库

## 个人电脑和小伙伴一起玩
如果你已经成功开好了一个服务器
``127.0.0.1``这个地址就是本地端，开服的人可以自己进本地端看看，有没有成功开启服务器

没有公网ip如何让自己的朋友也能进来

因为大部分人家里是没有公网ip的，所以需要用到内网穿透

进入[SAKURA FRP官网](https://www.natfrp.com/)(目前必须完成实名认证才允许使用中国大陆节点，认证需要支付1RMB)

注册登陆后左边菜单栏找到``软件下载``下载安装要用到的软件

``每日签到``可以获得免费的流量

官网的``管理面板``上也有[Minecraft的内网穿透教程](https://www.bilibili.com/video/BV1164y1c7iv/)空降5:30

打开安装好的内网穿透软件，创建隧道

``本地ip``填127.0.0.1

``端口``默认填25565

``隧道类型``选tcp

``服务器``自行选择线路

创建完毕后开启隧道，点开``日志``

```
TCP 类型隧道启动成功
使用 [*****] 来连接到你的隧道
或使用 IP 地址连接（不推荐）：[*****]

```
``日志``显示的两个地址都是可以用来连接服务器的

## 相关链接
[JAVA](https://www.oracle.com/java/technologies/downloads/)

[Fabric](https://fabricmc.net/use/)用于加载Mods 

[Carpet](https://www.curseforge.com/minecraft/mc-mods/carpet/files)地毯模组 

[Python官网](https://www.python.org/)

[MCDR](https://github.com/Fallen-Breath/MCDReforged)用于加载插件

[MCDR官方教程](https://mcdreforged.readthedocs.io/zh_CN/latest/quick_start.html)

[MCDR插件仓库](https://github.com/MCDReforged/PluginCatalogue/blob/catalogue/readme-zh_cn.md) 

[SAKURA FRP](https://www.natfrp.com/)用于内网穿透进行联机

[NATAPP](https://natapp.cn/)用于内网穿透进行联机
