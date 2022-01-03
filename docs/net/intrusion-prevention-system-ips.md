# 入侵防御系统(IPS)

> 原文:[https://www . geeksforgeeks . org/intrusion-prevention-system-IPS/](https://www.geeksforgeeks.org/intrusion-prevention-system-ips/)

入侵防御系统也被称为入侵检测和防御系统。它是一个网络安全应用程序，用于监控网络或系统活动中的恶意活动。入侵防御系统的主要功能是识别恶意活动，收集关于该活动的信息，报告该活动并试图阻止或阻止它。

入侵防御系统被认为是[入侵检测系统(IDS)](https://www.geeksforgeeks.org/intrusion-detection-system-ids/) 的扩展，因为 IPS 和 IDS 都针对恶意活动操作网络流量和系统活动。

IPS 通常记录与观察到的事件相关的信息，通知安全管理员重要的观察到的事件并生成报告。许多入侵防御系统也可以通过阻止检测到的威胁成功来对其做出响应。他们使用各种响应技术，包括入侵防御系统停止攻击本身、改变安全环境或改变攻击内容。

**入侵防御系统(IPS)分类:**
入侵防御系统(IPS)分为 4 种类型:

1.  **基于网络的入侵防御系统(NIPS):**
    它通过分析协议活动来监控整个网络的可疑流量。

2.  **无线入侵防御系统(WIPS):**
    它通过分析无线网络协议来监控无线网络中的可疑流量。

3.  **网络行为分析(NBA):**
    它检查网络流量，以识别产生异常流量的威胁，例如分布式拒绝服务攻击、特定形式的恶意软件和违反策略的行为。

4.  **基于主机的入侵防御系统(HIPS):**
    它是一个内置的软件包，通过扫描主机内发生的事件来操作单个主机进行可疑活动。

**入侵防御系统(IPS)技术比较:**
下表列出了各种 IPS 技术:

<figure class="table">

| 入侵防御系统技术类型 | 检测到的恶意活动类型 | 每个传感器的范围 | 强项 |
| 基于网络的 | 网络、传输和应用程序 TCP/IP 层活动 | 多个网络子网和主机组 | 只有 IDPS 能够分析最广泛的应用协议； |
| 无线的 | 无线协议活动；未经授权的无线正在使用的局域网 | 多个无线局域网和无线客户端组 | 只有 IDPS 能够预测无线协议活动 |
| 美国篮球职业联盟 | 网络、传输和应用程序 TCP/IP 层活动

这会导致异常的网络流量 | 多个网络子网和主机组 | 通常比其他人更有效识别侦察扫描和DoS 攻击，并在重建主要恶意软件感染 |
| 基于主机 | 主机应用程序和操作系统(OS)活动；网络，运输，和应用程序 TCP/IP 层活动 | 个体宿主 | 可以分析活动被端到端地传输加密通信 |

**入侵防御系统(IPS)的检测方法:**

1.  **基于签名的检测:**
    基于签名的 IDS 对网络中的数据包进行操作，并与预先构建和预先注定的攻击模式(称为签名)进行比较。

2.  **基于统计异常的检测:**
    基于异常的入侵检测系统监控网络流量，并将其与既定基线进行比较。基线将确定该网络的正常情况以及使用的协议。但是，如果没有智能配置基线，它可能会发出错误警报。

3.  **有状态协议分析检测:**
    这种 IDS 方法通过将观察到的事件与普遍接受的无害活动定义的预构建概要进行比较，来识别所陈述的协议的分歧。

**IPS 与 IDS 的比较:**
入侵防御系统(IPS)与入侵检测系统(IDS)的主要区别在于:

1.  入侵防御系统是串联的，能够主动防止或阻止检测到的入侵。
2.  入侵防御系统可以采取诸如发送警报、丢弃检测到的恶意数据包、重置连接或阻止来自违规 IP 地址的流量等操作。
3.  IPS 还可以纠正循环冗余校验(CRC)错误，对数据包流进行碎片整理，缓解 TCP 排序问题，并清理不需要的传输层和网络层选项。

</figure>