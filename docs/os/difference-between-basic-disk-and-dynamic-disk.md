# 基本盘和动态盘的区别

> 原文:[https://www . geesforgeks . org/基本磁盘和动态磁盘的区别/](https://www.geeksforgeeks.org/difference-between-basic-disk-and-dynamic-disk/)

**基本磁盘:**
基本磁盘是一种硬盘配置，可与 Windows 操作系统一起使用。为了管理硬盘上的所有分区和数据，使用普通分区表或逻辑驱动器。它们是 Windows 最常用的存储类型。它最多可以包含四个主分区，或者三个主分区和一个带有多个逻辑驱动器的扩展分区。

**要执行的操作:**

*   创建和删除主分区和扩展分区。
*   在扩展分区内创建和删除逻辑驱动器。
*   格式化分区并将其标记为活动的。

**动态磁盘:**
已经初始化为动态存储的磁盘称为动态磁盘。它比基本磁盘更灵活，因为它不使用分区表来跟踪所有分区。该分区可以通过动态磁盘配置进行扩展。它使用动态卷来管理数据。

**要执行的操作:**

*   创建和删除简单、跨区、剥离、镜像和 RAID-5 卷。
*   扩展简单卷或跨区卷。
*   修复镜像卷或 RAID-5 卷。
*   重新激活丢失或脱机的磁盘。

来看看基本盘和动态盘的区别:

<figure class="table">

| 没有 | 基本磁盘 | 动态磁盘 |
| --- | --- | --- |
| one | 基本磁盘使用在 MS-DOS 和 Windows 中找到的普通分区表来管理硬盘上的所有分区。 | 在动态磁盘中，硬盘分为动态卷。 |
| Two | 每个硬盘最多可以容纳 3 或 4 个分区，并且有一个辅助扩展分区。 | 在动态磁盘中，对主扩展分区和辅助扩展分区没有限制 |
| three | 在基本磁盘中，基本磁盘有两种分区方式:
1。MBR 分区
2。GPT 分区 | 在动态磁盘中，没有分区，它包含简单卷、跨区卷、剥离卷、镜像卷和 RAID-5 卷。 |
| four | 基本磁盘可以很容易地转换成动态磁盘，而不会丢失任何数据。 | 动态磁盘到基本磁盘的转换需要删除动态磁盘上的所有卷。 |
| five | 在基本磁盘中，不能更改或修改已经创建的分区。 | 在动态磁盘中，卷可以扩展。 |
| six | 它支持多引导配置。 | 它不支持多引导配置。 |
| seven | 它们与旧的操作系统兼容。 | windows 2000 及更高版本支持它们。 |

</figure>