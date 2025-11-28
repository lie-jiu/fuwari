---
title: tun无网络问题解决
published: 2025-11-28
description: tun无网络解决过程
image: ""
tags:
  - clash
  - tun
category: ""
draft: false
lang: ""
---
# 记一次开启tun无网问题解决过程

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
# 开始

打开Clash的虚拟网卡功能，发现无网络连接。

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