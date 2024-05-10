---
title: 儿童编程01 准备开发环境
date: 2024-05-05 16:51:33
categories: 
- 儿童编程
tags:
- SCAI
- StarCraft
- 星际争霸
---

# 学习目标
1. 准备编程所需要的各种软件（称之为**开发环境**）
2. 编写第一个能够控制游戏中SCV的程序（称之为**机器人或者bot**）

# 学习内容
1. 学会安装软件
2. 学会使用软件
3. 编写一个最简单的程序机器人（以后简称bot）并成功运行

# 开始学习
> StarCraft是星际争霸游戏，至于安装的其他软件，我们以后会慢慢说明他们的用途

## 安装游戏
1. 解压StarCraft.zip到桌面，最终游戏路径类似*C:\Users\【你的用户名】\Desktop\StarCraft*，我们将这个文件夹称为**游戏根文件夹**，这个名称我们后面会经常遇到。
   > 你可能看不见“.zip”字样，这没关系，只要文件名前面是StarCraft就可以

   > :point_right:还记得如何解压么？还记得如何查看文件夹路径么？
   > ![](scai01.png)|![](scai02.png)
   > --|--

## 安装Python
你学习的编程语言叫“Python”，中文意思是“蟒蛇”，我们通过安装Python来使用这门电脑编程语言。
1. 在**游戏根文件夹**下的software文件夹中找到*python-3.5.4.exe*并双击安装
![](scai03.png)
![](scai04.png)
![](scai05.png)
![](scai06.png)

## 安装BWAPI
我们的Python代码就是通过BWAPI这个软件来控制星际争霸游戏里面的各种元素（士兵、飞船、建筑等等）的。
1. 在**游戏根文件夹**下找到BWAPI_412.bat这个文件，双击完成注册表导入。当显示“操作成功完成”表示导入完成，这时点击键盘上任意按钮即可。(你可能不明白什么是注册表，没关系，我们以后也不会遇到他)
![](scai07.png)
![](scai08.png)
2. 在**游戏根文件夹**下找到双击BWAPI_412_Setup.exe这个文件,双击安装BWAPI
![](scai11.png)
![](scai12.png)
![](scai13.png)
![](scai14.png)
![](scai15.png)
![](scai16.png)
![](scai17.png)
![](scai18.png)
![](scai19.png)
![](scai20.png)
3. 安装完毕后**游戏根文件夹**会多出BWAPI和bwapi-data两个文件夹，其中BWAPI文件夹下的Chaoslauncher文件夹里面有个叫**Chaoslauncher.exe**的程序我们会经常用到。在桌面给他建个快捷方式吧。
> :point_right:还记得如何建快捷方式么？
![](scai21.png)
4. 下面设置下，让每次运行**Chaoslauncher.exe**快捷方式时都以“管理员权限”运行。（也就是让这个程序能完全控制定能，这样它才能帮我们控制游戏里的各种元素）。右键点击快捷方式并选择“属性”。
![](scai21a.png)
确保<font color=red>**以管理员身份运行此程序**</font>前面的勾选框是勾上的。
![](scai21b.png)

## 安装VSCode
1. 在**游戏根文件夹**下的software文件夹中找到VSCodeUserSetup-x64-1.87.2.exe，双击安装
![](scai22.png)
![](scai23.png)
![](scai24.png)
![](scai25.png)
![](scai26.png)
![](scai27.png)
![](scai28.png)

# 准备编程
作了这么多准备工作，终于到了我们的代码了。这里准备了一个例子代码，名字叫mybot，意思就是“我的机器人”。
1. 在**游戏根文件夹**下找到mybot，我们所有的代码都在这个文件夹下，后面我们把**游戏根文件夹**下面的mybot文件夹简称为**代码根文件夹**。这个名称我们后面会经常遇到。
![](scai29.png)
2. 在**代码根文件夹**下的scripts文件夹里双击运行venv.bat文件，当看到类似下面的界面，表示运行成功。
![](scai30.png)
3. 在**代码根文件夹**下的scripts文件夹里双击运行init.bat文件，当看到类似下面的界面，表示运行成功。
![](scai31.png)

# 开始编程
1. 右键点击**代码根文件夹**，选择“通过Code打开”
![](scai32.png)
2. 第一次这么操作时会出现下图界面，按截图勾选并点击按钮即可
![](scai33.png)
3. 点击![](scai36.png)可以浏览代码，此时再点击mybot.py就可以看到机器人的代码了。
![](scai34.png)
4. 点击![](scai37.png)可以安装插件，在**游戏根文件夹**下的software文件夹中找到ms-python-release-2020.8.6.vsix并点击“Install”
![](scai35.png)
![](scai38.png)
5. 当看到下述界面，表示一切就绪
![](scai39.png)

# 运行代码
1. 按F5键，将允许机器人代码，此时界面不断显示Game table mapping not found，这是机器人在等待游戏开始
![](scai40.png)
2. 还记得之前之前在桌面上创建的Chaoslauncher快捷方式么，这会终于用到它了。双击它，在随后弹出的界面中按下图选择，并最终点击“Start”
![](scai41.png)
![](scai42.png)
3. 在游戏里选择游戏内容，游戏用户和加载地图（这里我们选择map_01.scm这第一个也是最简单的教学地图），确保选择了“Use Map Settings”
![](scai43a.png)
![](scai43b.png)
![](scai43c.png)
![](scai44.png)
4. 到此为止，你得到了一个自动采矿的机器人。这个机器人就是有上面提到的mybot.py这个python代码控制的，当然，他现在还很低级，或者说和愚蠢，只会不停的采矿。随着你不断深入学习，完善他的功能，这个机器人将成长为智能、强大的战斗机器人，在星际争霸的游戏世界了大杀四方。
![](scai45.png)

<style>
td, th, tr {
   border: none!important;
}
</style>