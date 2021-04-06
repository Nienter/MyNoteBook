---
title: Android专家
date: 2021-03-17 12:00:19
tags:  android

---

<!-- toc -->

欢迎来到这里，你们都是有追求的人。 专家对应的级别为： 百度 T6 阿里 P7 腾讯 T3.1 滴滴 D8- 引言 在入门和高级路线里面，我们把该学的技术点基本都学完了。大家仔细想一下，高级和专家到底差多少？其实要论技术，未必差多少，但是却总是差那么一点感觉，这点感觉很重要。 在专家学习路线中，技术将不再那么重要，学习路线也不再那么具体，毕竟都要专家的人，还要靠我手把手教？这不是笑话嘛，而且手把手一定是教不出专家的，我指引一下，然后剩下靠自己感悟吧。 在我眼里，专家除了具有扎实的技术深度以外，还有一定的技术广度，以及不错的架构设计能力。但这只占50%，剩下50%是软技能，比如如何带人，如何写PPT，如何在公司里混？也许你想笑，但事实上，越是高级别越得会混，不然你是很难再向上发展的。 这部分内容比较虚，但是会对你职业生涯的后半段有很大帮助。

 ## 主线程消息循环（建议学习时间：1周） 

知识点：Binder原理、AIDL的使用、多进程的定义和特性 学习资料：

 ① Android开发艺术探索第10章 第三节【推荐理由】不解释。 ② [Android中为什么主线程不会因为Looper.loop()里的死循环卡死？ - 知乎](https://www.zhihu.com/question/34652589/answer/90344494) 【推荐理由】清晰正确，一切皆消息。 ③ [Android中MotionEvent的来源和ViewRootImpl - 任玉刚 - CSDN博客](https://blog.csdn.net/singwhatiwanna/article/details/50775201) 【推荐理由】以点击事件为例，进一步阐述皆消息。

## AMS（建议学习时间：4周）

 ① Android开发艺术探索 第9章【推荐理由】不解释。 ② Android内核剖析 第10章【推荐理由】我就是看这个学习的，我心中最好的资料。 ③Android进阶解密 第6章 【推荐理由】基于Android 8.0，结合上面的书再理解下。 PS：Android内核剖析已绝版，自己网上找PDF即可

## WMS（建议学习时间：4周）

 ① Android开发艺术探索 第8章【推荐理由】不解释。 ② Android内核剖析 第14章【推荐理由】我就是看这个学习的，我心中最好的资料。 ③ Android进阶解密 第8章 【推荐理由】基于Android 8.0，结合上面的书再理解下。

## PMS（建议学习时间：2周） 

① Android内核剖析 第16章【推荐理由】我就是看这个学习的，我心中最好的资料。 ② [[深入理解Android卷二 全文-第四章\]深入理解PackageManagerService - ...](https://blog.csdn.net/innost/article/details/47253179)【推荐理由】《深入理解Android》里面的内容 ③ 阅读PackageManagerService相关源码 

## SystemServer（建议学习时间：1周）

 ① [Android源码分析-Alarm机制与Binder的交互 - 任玉刚 - CSDN博客](https://blog.csdn.net/singwhatiwanna/article/details/18448997#t4)【推荐理由】任玉刚写的 ② Android进阶解密 第2章 【推荐理由】基于Android 8.0，结合上面的文章再理解下。 ③ 阅读SystemServer相关源码，了解系统服务的注册和运行 

## 复杂Gradle插件（建议学习时间：4周）

 ① [Android Gradle Plugin 源码解析（下）](https://mp.weixin.qq.com/s/DzuLtqx_CBFm9tJos9j2Ag)【推荐理由】Android gradle plugin源码解析。 ② [VirtualAPK/virtualapk-gradle-plugin at master · di...](https://github.com/didi/VirtualAPK/tree/master/virtualapk-gradle-plugin)【推荐理由】VirtualAPK gradle插件源码 ③ [GitHub - jasonross/NuwaGradle: gradle plugin wrote...](https://github.com/jasonross/NuwaGradle) 【推荐理由】nuwa gradle插件源码 说明：还需要查看Android源码的gradle分支，里面涉及到Android的构建细节，这样才能写出VirtualAPK类似的复杂插件。 

## 下载、阅读、编译Android源码、刷机（建议学习时间：2周）

 ① https://source.android.com/source/downloading.html【推荐理由】源码下载 ② [【Android源码查看工具】任玉刚在线视频教程 - CSDN学院-CSDN学院](https://edu.csdn.net/course/play/1923/29810)【推荐理由】源码阅读 ③ https://source.android.com/setup/build/building 【推荐理由】源码编译 ④ [https://source.android.com/setup/build/running.htm...](https://source.android.com/setup/build/running.html) 【推荐理由】刷机 说明：刷机最好用Google的nexus系列手机，将厂商设备驱动下载下来放到源码目录再进行编译，否则刷机后手机无法启动。

 专家路线的技术部分就到这里，推荐大家看完这三本书：《Android开发艺术探索》、《Android内核剖析》、《Android进阶解密》。 其他内容：都比较虚，有的是软技能，网上没有现成的资料，需要大家自己去学习去琢磨，专家不是手把手教出来的。我后面也会分享我的个人见解，这里给大家推荐几个相关的极客时间专栏（绝非广告），大家找时间读读： ① 程序员进阶攻略 ② 从0开始学架构 ③ 技术管理实战36讲

![img](E:\有道文件\yingyuwudi@163.com\ec21e98461db44539db8bfb1acb2d48c\ekosogydiu_.jpeg)