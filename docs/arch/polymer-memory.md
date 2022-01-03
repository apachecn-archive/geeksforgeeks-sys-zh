# 聚合物记忆

> 原文:[https://www.geeksforgeeks.org/polymer-memory/](https://www.geeksforgeeks.org/polymer-memory/)

**半导体存储器**是用于数字数据存储的数字电子半导体器件，例如计算机存储器，其中数据存储在硅集成电路存储器芯片上的金属-氧化物-半导体(MOS)存储单元内。**聚合物存储器**暗示了新的存储器创新，利用导电聚合物而不是硅基结构来存储数据。聚合物是适应性很强的有机材料，由长的单分子链组成。聚合物是基本的电子材料，可以加工成液体。利用薄膜存储技术，聚合物被用于各种工业标准过程。

一种被称为 **PEDOT(聚乙烯二氧噻吩)**的聚合物是一种不寻常的塑料，因为它在低电压下导电，这使得这种聚合物适用于各种工业过程中的防静电涂层。后来发现，在高脉冲电流下，它会变成非导电状态(充当绝缘体)。基于 PEDOT 的存储器用于将计算机化的数据存储为 0 和 1。通过堆叠多层内存，一个立方厘米的小装置可以容纳多达一千兆字节的数据，并且足够小，足以与光盘和 DVD 相媲美。

**聚合物记忆是如何工作的:**
基于聚合物的记忆背后的基本原理是聚合物链所具有的偶极矩，因为该偶极矩，聚合物表现出不同的电导率，并且当施加电场时，聚合物局部偶极矩被建立。**偶极矩**建立当电场作用于含有正负电荷的固体时，正电荷向场的负端方向移动，而负电荷向场的正端方向移动，从而建立了偶极子。与硅器件相比，聚合物存储器以完全不同的方式存储数据。Coatues 芯片不是将 0 和 1 编码为存储在电池中的电荷的量度，而是基于聚合物的电阻来存储数据。Coatue 将每个存储单元制作成夹在两个电极之间的聚合物。为了启动该电池框架，在顶部和底部电极施加电压。利用电场降低聚合物的电阻，从而扩大其传导电流的能力；聚合物保持其状态，直到施加相反极性的电场，使其电阻恢复到原来的水平。不同的导电状态构成了数据位。

**聚合物记忆的特征:**

*   存储的每一位都是零晶体管。
*   内存是非易失性的。
*   微秒初始读数。写入速度快于 [NAND 和](https://www.geeksforgeeks.org/introduction-of-logic-gates/)NOR 闪存。
*   基础准备，简单配合不同的 [CMOS](https://www.geeksforgeeks.org/what-is-the-need-of-cmos-battery-in-computers/) 。
*   不需要单元备份控制或刷新。
*   工作温度范围在–40 至 110℃之间

**聚合物存储器的优势:**

*   塑料记忆很快。实验室组装的具有 1GB 存储容量的小工具产生的读/写过程持续时间比 CompactFlash 快几倍(10 倍)，compact flash 通常为 10MB/s 读取，1-4MB/s 合成，因此提供了快速的读写速度。
*   低功耗。
*   它需要的晶体管要少得多，1GB 的存储容量通常只有 50 万个，而硅的存储容量为 15-65 亿个。
*   它可以垂直堆叠在一个项目中，产生 3D 空间利用率；硅片必须彼此相邻放置。
*   制作简单:使用喷墨打印机将流体聚合物电路喷洒到表面上
*   薄膜框架需要大约 50 万个晶体管来存储每千兆字节的内存。传统的硅基框架需要 15 亿到 65 亿个晶体管才能实现同样的千兆字节。

**聚合物记忆的局限性:**

*   将聚合物存储器转变为商用存储器是一项繁琐的任务，因为存储器技术不仅在存储容量上竞争，而且在能耗、速度和稳定的质量等方面也是如此。
*   它可以读很多次，但只能写一次。
*   他们指出，在新的存储材料能够与硅的高性能相抗衡之前，它们可能会被限制在利基应用中。