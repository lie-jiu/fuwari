---
title: 解决tun无网络问题的两种方法
published: 2025-11-28
description: tun无网络解决过程
image: ""
tags:
  - clash
  - tun
category: ""
draft: false
lang: zh_CN
---

## 前言
---

系统版本	Windows 11 专业版

版本号	25H2

安装日期	‎2025/‎10/‎10

操作系统版本	26200.7171

体验	Windows 功能体验包 1000.26100.265.0

---

软件 [clash-verge-rev](https://github.com/clash-verge-rev/clash-verge-rev)


Verge Version: 2.4.4+autobuild.1122.45020fc


Running Mode: Service


Is Admin: false

---
### 可能影响的操作
[ZyperWin++](https://github.com/ZyperWave/ZyperWinOptimize)的基础优化功能与卸载edge浏览器及其核心。保留WebView2。

clash的虚拟网卡在我使用不忘初心的精简版系统是能够正常使用的，

且能够在任务管理器中看到虚拟网卡。

但是在切换为win11原版时就不行了

---
:::tip
建议使用方法二，点击目录跳转。
:::
# 开始

## 方法一

首先打开Clash的虚拟网卡功能

打开控制面板
![](src/content/posts/assets/images/PixPin_2025-11-28_12-18-49.png)
点击*网络和Internet*

![](src/content/posts/assets/images/PixPin_2025-11-28_12-19-17.png)
打开*网络和共享中心*

![](src/content/posts/assets/images/PixPin_2025-11-28_12-19-46.png)

点击*Mihomo*

![](src/content/posts/assets/images/PixPin_2025-11-28_12-20-14.png)
点击*属性*
![](src/content/posts/assets/images/PixPin_2025-11-28_12-20-30.png)
点击上方选项卡的*共享*

![](src/content/posts/assets/images/PixPin_2025-11-28_12-20-50.png)
1.勾选 *允许其他网络用户通过此计算机的Internet连接来连接* 选项

2.选择*WLAN*

这个时候你去测试发现依旧无网络连接，别急。

我来教你，现在再把 *允许其他网络用户通过此计算机的Internet连接来连接* 选项取消勾选。

你就会发现虚拟网卡模式可以正常联网了。

且代理功能正常使用。

然而任务管理器并没有显示Tun的网络。

### 方法一总结

每次重启都需要开关一次共享，不推荐。

---

## 方法二

**管理员模式**打开Clash

打开Clash虚拟网卡功能

![](src/content/posts/assets/images/PixPin_2025-11-28_13-06-44.png)
点击设置图标

![](src/content/posts/assets/images/PixPin_2025-11-28_13-07-15.png)
模式堆栈选择*Mixed*

开关*虚拟网卡模式*开关后，检查有没有网络连接

如果可以正常使用了，那么本章对你来说已经结束了。

---

如果没有就前往*Windows 安全中心*

![](src/content/posts/assets/images/PixPin_2025-11-28_13-20-29.png)
点击*允许应用通过防火墙*
![](src/content/posts/assets/images/PixPin_2025-11-28_13-22-03.png)
点击*更改设置*


勾选名称带有*Mihomo*应用。


如果没有找到，请使用下面的允许其他应用。

点击下方添加

找到clash的安装路径


默认路径
```
C:\Program Files\Clash Verge
```

![](src/content/posts/assets/images/PixPin_2025-11-28_13-28-00.png)
建议勾选这三个应用。
其中*verge-mihomo*必须勾选