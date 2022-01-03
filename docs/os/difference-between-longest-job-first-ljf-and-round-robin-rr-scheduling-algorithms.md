# 最长作业优先(LJF)和循环调度(RR)调度算法之间的差异

> 原文:[https://www . geesforgeks . org/最长作业优先 ljf 和循环调度算法之间的差异/](https://www.geeksforgeeks.org/difference-between-longest-job-first-ljf-and-round-robin-rr-scheduling-algorithms/)

**1。最长作业优先(LJF) :**
最长作业优先(LJF)基于进程的突发时间。进程根据其突发时间被放入就绪队列。在该算法中，首先处理突发时间最大的进程。仅比较那些在该时间之前存在或已经到达的进程的突发时间。它本质上也是非先发制人的。其抢先版被称为[最长剩余时间优先(LRTF)算法](https://www.google.com/amp/s/www.geeksforgeeks.org/longest-remaining-time-first-lrtf-cpu-scheduling-algorithm/amp/)。

该算法的主要缺点是，对于给定的一组流程，它给出了非常高的平均等待时间和平均周转时间，因此降低了系统的有效性。也可能导致护航效应。

**注意–**
如果两个进程具有相同的突发时间，则使用 FCFS 断开连接，即先到达的进程先被处理。

**2。[循环调度算法](https://www.geeksforgeeks.org/program-round-robin-scheduling-set-1/) :**
循环调度算法是专门为分时系统设计的。进程被放入就绪队列，在这种情况下是一个循环队列。在这种情况下，定义了一个称为时间量子的小时间单位。该算法从队列中选择第一个进程，并在时间段定义的时间内执行它。如果进程的突发时间小于时间量，则中央处理器执行下一个进程，但是如果它的突发时间高于时间量，则该进程被中断，并且为相同的时间量执行下一个进程。如果一个进程被中断，那么就会发生一个上下文切换，并且这个进程会被放回队列的尾部。本质上是先发制人。

该算法主要依赖于时间量子。非常大的时间量使得 RR 与 FCFS 相同，而非常小的时间量将导致开销，因为上下文切换将在非常小的间隔后一次又一次地发生。

这种算法的主要优点是所有进程一个接一个地执行，不会导致进程饥饿或等待相当长的时间才能执行。

最长作业优先(LJF)和循环调度(RR)算法的区别如下:

<center>

| 最长工作优先(LJF) | 循环赛 |
| --- | --- |
| 最长作业优先(LJF)根据突发时间执行进程，即按照突发时间的降序。 | 循环调度根据定义的时间量执行进程，即每个进程执行固定的时间量。 |
| LJF 也是非抢先的，但是它的抢先版本也被称为最长剩余时间优先(LRTF)算法。 | 循环赛本质上是先发制人的。 |
| 给定流程集的平均等待时间和平均周转时间非常大。 | 给定进程集的平均等待时间非常短，并且取决于时间量。 |
| LJF 算法很难实现。 | 实现 RR 相当容易。 |
| 短进程可能永远不会被执行，系统可能会继续执行较长的进程，用户可能会觉得在多用户系统的情况下，他的工作被忽略了。 | 每个进程都被执行，每个用户都觉得自己的工作正在完成，因为中央处理器给了每个进程相等的时间。 |
| 就 LJF 而言，非常长的等待时间导致处理缓慢，降低了系统的效率。 | 在 RR 的情况下，如果时间量非常小，那么在非常短的时间间隔之后，上下文切换会一次又一次地发生，这导致开销。 |

</center>