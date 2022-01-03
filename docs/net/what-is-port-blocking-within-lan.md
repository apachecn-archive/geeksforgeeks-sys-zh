# 什么是局域网内的端口阻塞？

> 原文:[https://www . geesforgeks . org/什么是局域网内端口阻塞/](https://www.geeksforgeeks.org/what-is-port-blocking-within-lan/)

**端口阻塞**是互联网服务提供商(ISP)通过使用端口号和传输协议来识别和阻塞互联网流量的动作。

**局域网内端口阻塞**是指限制用户访问局域网内的一组服务。这可能包括阻止物理端口，如通用串行总线、可移动设备、数字视盘/光盘、软盘、智能手机和许多此类即插即用设备。

### **局域网内端口阻塞的需要**

考虑在您的网络中启用 DHCP 服务的情况。现在，如果任何拥有笔记本电脑的用户将局域网电缆与您的设备连接起来，通过这种连接，该用户可以从 [DHCP](https://www.geeksforgeeks.org/dynamic-host-configuration-protocol-dhcp/) 获得您的 IP 地址，并可以访问您的网络资源。因此，为了避免这种情况，如果可以在局域网内启用端口安全，那么每当端口与媒体访问控制地址不匹配时，交换机将关闭端口，匿名用户将无法获得该 IP。

**示例:**假设我们想要阻塞一个具有特定 [MAC 地址](https://www.geeksforgeeks.org/introduction-of-mac-address-in-computer-network/)的交换机端口。假设我们有一台 8 端口交换机，现在如果我们连接一台 mac 地址为 2c.54.91.88.c9.e3 的机器，并且我们用该地址阻塞交换机端口，那么只要检测到除上述 MAC 地址之外的外部 MAC 地址，您的交换机就会切断连接，您的机器就会受到保护。

数据传输通过一些特定的端口进行。为了路由流量，计算机使用端口号。一些端口使用[传输控制协议(TCP)](https://www.geeksforgeeks.org/what-is-transmission-control-protocol-tcp/) ，而一些使用[用户数据报协议(UDP)](https://www.geeksforgeeks.org/user-datagram-protocol-udp/) 。这些协议决定了数据传输，即一旦计算机通过网络相互连接，数据应该如何传输。

### **关闭计算机端口的步骤**

**1。**转到**开始- >控制面板- >系统和安全- > Windows 防火墙。**

**2。**选择“**高级设置”- >“入站规则”**(阻止入站端口)或“**出站规则”**(阻止出站端口)。

**3。**从选项中选择“**新规则**”选择“**端口**，点击**下一步**。

**4。**选择 **TCP** 或 **UDP** ，点击**特定本地端口**。

**5。**输入端口号，点击**下一步**。

**6。**点击**阻断连接**，然后点击**下一步**。选择规则适用的网络位置(公共、私有、域)，然后单击“**下一步**”。

**7。**创建规则名称并为其添加描述。点击**完成**以封锁电脑上的端口。

### **阻塞的影响**

许多端口通常与 windows 应用程序相关联。由于缺乏系统管理和网络安全方面的专业知识，他们吸引了黑客。

这些端口使用的服务并不意味着在广域网或管理域之间使用；因此，阻塞端口不会影响正确设计的应用程序，只有少数较旧的应用程序除外。

### **优势**

**1。**局域网内的端口阻塞有助于防止不需要的数据进入您的计算机。

**2。**更快的网络。

**缺点:**

**1。**应用程序功能不正常，因为应用程序无法访问正常工作所需的端口。

**2。**它使设计和开发应用程序的过程变得复杂，并对产品或应用程序是否能正常工作产生不可靠性。