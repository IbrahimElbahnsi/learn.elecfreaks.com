﻿---
sidebar_position: 3
sidebar_label: 案例03 动态调节植物生长环境光照
---
# 案例03 动态调节植物生长环境光照

## 简介

本课程将向学生介绍八爪鱼系列的 8 颗彩虹灯环器件的使用和编程方式以及 micro:bit V2 的光线传感器编程方式。学生将使用 8 颗彩虹灯环改变植物生长环境的光照，包括光照强度和颜色，以及用 micro:bit V2 测量日光的光线强度等。

## 教学目标

- 了解八爪鱼系列的 8 颗彩虹灯环的连接方式以及编程方式 。
- 了解使用 micro:bit V2 的光线传感器的编程方式。

## 教学准备

在开始教学之前，请确保您已经准备好以下必要的物品：

|                             图片                             |                名称                |
| :----------------------------------------------------------: | :--------------------------------: |
| ![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-hardware-introduction-014.png) |             micro:bit              |
| ![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-hardware-introduction-020.png) |              IOT:bit               |
| ![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-hardware-introduction-030.png) |          3V Relay Module           |
| ![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-hardware-introduction-040.png) |       3V Vertical Water Pump       |
| ![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-hardware-introduction-050.png) |        8 Rainbow LED Light         |
| ![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-hardware-introduction-060.png) | Octopus Soil Moisture Sensor Brick |
| ![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-hardware-introduction-070.png) |        Octopus Light Sensor        |
| ![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-hardware-introduction-078.png) |          Greenhouse Model          |
|                                                              |                                    |
| ![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-hardware-introduction-090.png) |         Double-sided Tape          |
| ![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-hardware-introduction-011.png) |          Flat Screwdriver          |
| ![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-hardware-introduction-012.png) |                 PC                 |
| ![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-hardware-introduction-013.png) |             USB Cable              |
| ![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-hardware-introduction-015.png) |           4P公对母杜邦线           |
| ![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-hardware-introduction-016.png) |           5P母对母杜邦线           |

这些物品将为您提供一个完整的体验，确保您可以顺利地进行后续的操作和学习。如果您已准备好以上内容，我们可以继续进入下一步。

## 教学过程

### 课程引入

在前面的课程中，我们得到了植物生长环境中的温度数据以及土壤湿度数据并通过 ThingSpeak 平台清楚的看到数据的变化，但是，植物在生长过程中，光照也是必不可少的条件之一，所以，在本节课程中，我们将使用 micro:bit V2 的光线传感器检测日光的光线强度以及使用 8 颗彩虹灯环改变植物光照强度和光线颜色。

现在，那我们开始吧！

### 探究活动

- 如何通过编程控制 8 颗彩虹灯环的颜色和光线强度？
- 如何使用 micro:bit V2 的光线传感器测量日光强度？

## 组装智能温室大棚


将micro:bit 插入IOT:bit 扩展板，在IOT:bit 扩展板背面贴上无痕胶后，固定到温室大棚模型底座上面，如下图所示：

![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-hardware-introduction-017.png)

将3V水泵和3V继电器放置如下图所示位置：

![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-hardware-introduction-018.png)

将适量的土壤倒入温室基地植物生长池和放置种子，将土壤湿度传感器插入土壤中。

![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-hardware-introduction-019.png)

将8颗彩虹灯环固定到透明外罩的顶部。

![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-hardware-introduction-021.png)

使用无痕胶将光线传感器黏贴到温室大棚模型透明外罩顶部，如下图所示。

![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-hardware-introduction-022.png)

将土壤湿度传感器的连接线、8颗彩虹灯环的连接线、光线传感器的连接线、3V水泵软管，按如下图所示穿过温室大棚透明外罩孔，然后将其放下：

![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-hardware-introduction-023.png)

按下方连线图所示，将3V水泵、3V继电器、土壤湿度传感器、光线传感器和8颗彩虹LED灯连接到 IOT:bit 扩展板上。

|     元器件     | IOT:bit 对应引脚 |
| :------------: | :--------------: |
|  8颗彩虹LED灯  |        P1        |
| 土壤湿度传感器 |        P2        |
|   光线传感器   |        P3        |
|    3V继电器    |        P9        |

​

![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-hardware-introduction-026.png)

将适量的水倒入温室底部水槽。

![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-hardware-introduction-024.png)

将电源连接到 IOT:bit 扩展使用 USB 数据线连接板，然后打开电源开关。

![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-hardware-introduction-025.png)

### 代码编程

#### 添加软件库

进入“[makecode.microbit.org](https://makecode.microbit.org/)”，点击“**New Project**”。

![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-programming-preparation-01.png)



在弹出窗口中输入项目名称并点击“**Create**”。

![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-programming-preparation-02.png)



在打开的编程界面中，点击编程积木抽屉中“**Extensions**”。

![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-programming-preparation-03.png)



打开拓展页面后，在搜索栏中输入“**iot-environment-kit**”，点击搜索，在搜索结果中选择 “**iot-environment-kit**” 编程积木库。

![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-programming-preparation-04.png)



添加成功后，可以在编程积木抽屉栏看到 “**ESP8266_IoT**、**OLED**、**RTC1307**、**Octopus**”。

![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-programming-preparation-05.png)

同样，还需要添加官方的 “**neopixel**” 库文件。

![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-programming-preparation-16.png)



添加成功后，可以在编程积木抽屉栏看到“**Neopixel**”。

![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-programming-preparation-17.png)



### 示例代码



![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-programming-case03-1.png)

请参考程序链接：https://makecode.microbit.org/_gbvK2JeKYEsp。

### 下载程序

使用 USB 数据线连接电脑和 micro:bit V2。

![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-programming-preparation-06.gif)

连接成功后，电脑上会识别出一个名为 **MICROBIT** 的盘符。

![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-programming-preparation-07.png)

点击左下角的![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-programming-preparation-08.png)，选择 **Connect Device**。

![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-programming-preparation-09.png)

点击![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-programming-preparation-10.png)。

![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-programming-preparation-11.png)

点击![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-programming-preparation-12.png)。

![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-programming-preparation-13.png)



在弹出窗口选择 “**BBC micro:bit CMSIS-DAP**”，然后选择 “**Connect**”，至此，我们的 micro:bit 就已经连接成功。

![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-programming-preparation-14.png)

点击下载程序。

![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-programming-preparation-15.png)

### 团队合作与展示

学生分成小组，共同完成智能温室大棚的安装和程序编写。

鼓励学生之间相互合作、交流和分享经验。

每个小组有机会向其他小组展示他们制作的智能温室大棚，并演示。

**预期效果：** 随着植物周围环境的光线强度变化，8 颗彩虹灯环发出不同亮度的光线以及不同颜色的光。

![](https://wiki-media-ef.oss-cn-hongkong.aliyuncs.com/docs/microbit/wisdom-life/microbit-smart-greenhouse-kit/images/microbit-greenhouse-case3.gif)

### 总结与反思

回顾课程内容，提醒学生掌握了哪些知识和技能。

引导学生讨论他们在制作过程中遇到的问题和困难，以及如何解决这些问题。

引导学生思考程序的优化和改进方向，比如利用 micro:bit 还能制作哪些有趣的案例。

## 扩展知识

**植物光照调整**：在植物生长过程中，光照强度和波长是非常重要的环境因素，它们可以直接影响植物的生长和发育。为了使植物生长最好，需要动态调整光照强度和波长。

首先，对于光照强度而言，需要根据植物的种类和生长阶段来调整。一般来说，植物在生长旺盛期需要较强的光照强度，以促进光合作用的进行，加速植物的生长。但是，光照强度也不能过高，否则会导致植物受到光抑制，甚至引起植物的死亡。因此，在调节光照强度时，需要根据植物的具体情况来决定。

其次，对于波长而言，不同植物对光的波长有不同的需求。一般来说，蓝光和红光对植物的生长和发育有重要作用。蓝光有助于植物的形态建成和光合作用的进行，而红光则有助于植物的生长和发育。因此，在调节波长时，需要根据植物的具体需求来选择不同的波长组合。

此外，除了调节光照强度和波长外，还需要注意光照时间和温度等其他环境因素。光照时间的长短也会影响植物的生长和发育，而温度的高低也会对植物的光合作用和呼吸作用产生影响。因此，在调节光照强度和波长的同时，也需要合理控制其他环境因素。

综上所述，要使植物生长最好，需要动态调整光照强度和波长，以及其他相关环境因素。具体的调整方法需要根据植物的种类和生长阶段来决定。
