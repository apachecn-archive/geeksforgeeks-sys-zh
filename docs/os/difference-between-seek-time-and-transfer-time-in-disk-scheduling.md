# 磁盘调度中寻道时间和传输时间的差异

> 原文:[https://www . geesforgeks . org/磁盘寻道时间和传输时间的差异调度/](https://www.geeksforgeeks.org/difference-between-seek-time-and-transfer-time-in-disk-scheduling/)

在硬盘中，存在一个磁头，它应该从磁盘中写入或读取，在本文中，我将把它称为*磁头*。

**寻道时间:**
是磁盘磁头从磁盘上的一个磁道移动到另一个磁道所用的时间。发送读/写请求时，寻道时间会因磁头当前所处的位置而有很大差异，因此平均寻道时间的使用更为广泛。

为了更清晰的画面，考虑一个同心圆的硬盘，叫做*磁道*，假设你想取一些数据。寻道时间是磁头从其当前磁道移动到数据所在磁道所需的时间，即使在此之后，它也可能需要等待一段时间，因为数据位于磁道的另一端，这种延迟称为旋转延迟，但这不计入寻道时间。

取决于:

*   读/写磁头速度
*   当前位置和最终位置之间的距离

**传输时间:**
传输时间是从磁盘传输数据所花费的时间。它根据磁盘的旋转速度而变化，磁盘旋转得越快，我们读取数据的速度就越快，根据一个磁道上的字节数(也称为磁盘密度)，我们传输数据的速度就越快，因此传输时间就越短。

取决于:

*   圆盘的转速，越快越好
*   磁道和扇区密度，越多越好
*   要传输的数据量

<figure class="table">

| 没有 | 寻道时间 | 转移时间 |
| --- | --- | --- |
| one | 磁头从当前磁道移动到有数据的磁道所用的时间。 | 将数据从磁盘传输到主机系统所需的时间。 |
| Two | 根据当前位置和最终位置之间的距离以及指示的行进方式，可能会有很大的不同。 | T = b/rN
T 是传输时间，b 是要传输的字节数，N 是磁道上的字节数，r 是转速，单位为 Rps |
| three | 测量平均寻道时间 | 单位时间内传输的数据量，即秒 |
| four | 通常在 10-20 毫秒之间，取决于转速和驱动器等级 | 传输 30-60MB 的数据大约需要 1 秒钟 |

</figure>