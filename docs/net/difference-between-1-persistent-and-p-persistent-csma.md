# 1 持久和 p 持久 CSMA 的区别

> 原文:[https://www . geesforgeks . org/difference-1-persistent-和-p-persistent-csma/](https://www.geeksforgeeks.org/difference-between-1-persistent-and-p-persistent-csma/)

先决条件–[载波侦听多路访问(CSMA)](https://www.geeksforgeeks.org/carrier-sense-multiple-access-csma/)
**1。1-持久 CSMA :**
在 1-持久 CSMA 中，站连续感测信道以检查其状态，即空闲或忙碌，以便它可以传输数据。如果频道忙，电台将等待频道空闲。当站发现空闲信道时，它以概率 1 在信道间无任何延迟地发送帧。由于概率 1，它被称为 1-持久 CSMA。这种方法的问题是冲突的可能性很大，因为两个或多个站可以在空闲状态下找到信道并同时传输帧。当冲突发生时，站必须等待随机时间，使信道空闲并重新开始。

![](img/d435c8a2fd20c85986e78cf284d04b6c.png)

<center>**Figure –** 1-persistent CSMA</center>

**2。p-持久 CSMA :**
当一个信道有时隙并且该时隙持续时间等于或大于该信道的最大传播延迟时间时，使用 p-持久 CSMA。当站准备发送帧时，它将感知信道。如果发现频道忙，电台将等待下一个时隙。但是如果发现信道空闲，站以概率 p 立即发送帧。因此，站等待剩余概率，即等于 1-p 的 q，以开始下一个时隙。如果发现下一个时隙也是空闲的，站发送或以概率 p 和 q 再次等待，这个过程重复进行，直到帧被发送或另一个站开始发送。

![](img/f4102f99e176ba359a5651cd243e1629.png)

<center>**Figure –** p-persistent CSMA</center>

**1 持久和 p 持久 CSMA 的区别:**

<center>

| 基础 | 1-持久的 CSMA | 持久性 CSMA |
| --- | --- | --- |
| 载波侦听 | 当信道空闲时，它将以概率 1 发送。 | 当信道空闲时，它将以概率 p 发送。 |
| 等待 | 它将持续检测帧传输的信道。 | 它将等待下一个传输帧的时隙。 |
| 碰撞的机会 | 在这种方法中，观察到的碰撞数量最多。 | 在这种方法中，碰撞的机会比在 1-persistent 中少。 |
| 利用 | 它的利用率高于 ALOHA，因为只有在空闲状态下发现信道时才会发送帧。 | 它的利用率取决于概率 p。 |
| 延迟低负载 | 它很小，因为帧只在空闲状态下发送。 | 当概率 p 较小时，该值较大，因为站不会总是在信道空闲状态下发送。 |
| 延迟高负载 | 由于碰撞，它很高。 | 当发现信道处于空闲状态时，发送的概率 p 较小时，该概率较大。 |

</center>