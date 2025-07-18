---
title: RPCS3游戏安装说明
author: AaronP
tags:
  - Tutorial
---

# RPCS3游戏安装说明

本教程为RPCS3游戏安装操作步骤说明。

如遇到问题、希望进行反馈、亦或是有任何建议，请加入测试QQ群：591676099

[微云分流地址](https://share.weiyun.com/SDJaXOmH)

## 目录



## 全部所需文件SHA1哈希

请预先准备好原游戏镜像，以下为本教程使用的文件的SHA1哈希。其中游戏镜像部分哈希仅供参考。

### 模拟器&固件

- PS3UPDAT.PUP：093F8698B54B78DCB701DE2043F82639DE51D63B
- rpcs3-v0.0.29-15711-e26d4e17_win64.7z：241B7D7AB81B5F990939A7115E6DD8EB08831FCC

### 原游戏镜像（仅供参考）

- THE iDOLM@STER One For All [BLJS10260].iso：296E83EEF8732FE15CBA8F70229AB37870905A0B (4.96 GB)
- THE iDOLM@STER One For All Patch 1.07.pkg：3AE25C229C86D18BBD13024C495616887AD55FC4 (220 MB)
- THE iDOLM@STER One For All [BLJS10260][DLC].pkg：BB646967F05019AE90DC9551A32D1216CE79F0D6 (4.19 GB)


## RPCS3说明

- RPCS3建议不修改画面设置，已证实调整画面和滤镜设置可能导致游戏贴图渲染错误。
- RPCS3建议使用**PS3/4/5或PlayStation兼容手柄**，**有线**连接PC进行游戏，**不要使用**Xbox或类Xbox键位手柄，**不要无线连接PC**



## RPCS3 原版游戏安装说明

PS3实机玩家请按照自己固件的安装方式进行安装。熟悉RPCS3的玩家可以仅看本文游戏设置部分的内容。

### 固件安装&游戏设置

解压`rpcs3-v0.0.29-15711-e26d4e17_win64.7z`，模拟器目录内双击`rpcs3.exe`启动模拟器，关闭初次启动的欢迎界面，点击左上角 File -> Install Firmware，选择提供的固件文件 `PS3UPDAT.PUP`， RPCS3 将自动编译安装PS3固件，这个过程耗时视CPU性能决定，耗时3-15分钟不等。

![intsall-firmware](/images/intsall-firmware.jpg)


由于不同渲染设置可能造成图像问题，且不同地域的手柄○/× 按钮功能不同，建议的RPCS3点击Configuration -> CPU ，逐个对照下列设置(没提供图示的请保持默认)。

- CPU：LLVM动态重编译

![CPU](/images/CPU.jpg)

- GPU：调整渲染器和分辨率，图形设备选择PC的独立显卡

![GPU](/images/GPU.jpg)

- Audio：采用兼容性最好的立体声设置

![Audio](/images/Audio.jpg)

- System：地区请选择Japan, 确认按键选择circle (○键)

![System](/images/System.jpg)

- Advanced：高级设置

![Advanced](/images/Advanced.jpg)

- Emulator：模拟器运行设置，关闭部分信息提示，开启全屏游戏，提升沉浸度

![Emulator](/images/Emulator.jpg)

- GUI：关闭模拟器自动更新，不建议更新模拟器

![GUI](/images/GUI.jpg)

- 手柄调试：RPCS3点击Configuration -> Pads

![refresh](/images/pads1.png)

Handlers 选择自己插入的手柄类型(PS3手柄 -> DualShock3, PS4及PlayStation4兼容手柄 -> DualShock4, PS5手柄 DualSense)。推动左右摇杆，右下角可看到感应点，检测手柄有效性。

![pads2](/images/pads2.jpg)


### 安装游戏


解压原游戏镜像`THE iDOLM@STER One For All [BLJS10260].iso`，将解压得到的完整文件夹复制到模拟器目录内的`/games/`目录下。然后单击模拟器界面的refresh按钮，此时偶像大师OFA原始镜像完成安装，界面中出现游戏。

![refresh](/images/refresh.jpg)


点击左上角 File -> Intsall Packages/Raps/Edats，选择版本更新文件`THE iDOLM@STER One For All Patch 1.07.pkg` 安装游戏的版本更新，此时游戏的Version列将更新为`01.07`，然后再次点击点击左上角 File -> Intsall Packages/Raps/Edats，选择DLC文件`THE iDOLM@STER One For All [BLJS10260][DLC].pkg`，安装完整DLC。(如果自己的镜像是1-9，10-14两个DLC pkg文件，则按顺序依次安装两个pkg即可)

![install-pkg](/images/install-pkg.jpg)


此时你已经完成原版游戏的安装。接下来请参考[汉化补丁说明](https://imas-ofa.com/2023/12/12/PatchTutorial.html)进行游戏汉化操作。