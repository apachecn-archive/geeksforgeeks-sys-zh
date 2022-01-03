# 量子位操作系统介绍

> 原文:[https://www.geeksforgeeks.org/introduction-of-qubes-os/](https://www.geeksforgeeks.org/introduction-of-qubes-os/)

**Qubes OS** 是桌面[操作系统](https://www.geeksforgeeks.org/operating-systems/)，旨在通过隔离提供安全。它在虚拟化的帮助下提供了不同的环境。没有完美的无 bug 桌面环境，因为像 windows 这样的桌面环境是数百万行代码和数十亿[软件/硬件](https://www.geeksforgeeks.org/difference-between-hardware-and-software/)交互的结果。

因此，这些交互中的一个关键错误足以让恶意软件控制机器。

在这种情况下，代理、虚拟专用网或任何其他方法都无法保存您系统的数据，也无法保护您免受网络攻击。

量子位有助于用户保持安全。

**为什么是量子位？**
为了保证桌面的安全，Qubes OS 为不同的任务提供了不同的环境，例如为控制硬件提供了不同的环境，为控制软件提供了不同的环境，为交互用户提供了不同的环境，为连接设备提供了不同的环境。因此，如果其中一个组件遭到破坏，恶意软件将只能访问该环境中的数据，因此由于不同环境之间的隔离，其余数据将被保存。

在量子位中，隔离是二维的，硬件控制器可以隔离成功能域(例如网络域、通用串行总线控制器域)，而用户的数字生活是由不同信任级别的躯体决定的。

例如工作域(最受信任)、购物域、随机域(不太受信任)。

这些域中的每一个都在单独的虚拟机中运行。

**特征:**

1.  强隔离:它有助于隔离软件，就像它们安装在单独的机器上一样。它使用光伏或 HVM 虚拟化技术进行隔离。
2.  多操作系统:它允许用户使用多种操作系统，如 Fedora、Debian 或 windows。
3.  控制器隔离:通过网卡和 USB 控制器的隔离，帮助用户确保设备操作的安全。
4.  U2F 代理:使用 Qubes U2F 代理有助于使用双因素认证。
5.  开源:这是一个开源环境，即允许用户使用、复制或修改量子位操作系统，并鼓励用户这样做。
6.  一次性虚拟机:它创建一次性虚拟机。一次性虚拟机是轻量级虚拟机，创建速度很快，关闭后就会消失。它们通常被创建来托管单个应用程序，如查看器、编辑器或 web 浏览器。