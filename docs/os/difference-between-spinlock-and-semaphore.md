# 自旋锁和信号量的区别

> 原文:[https://www . geeksforgeeks . org/spin lock 和 semaphore 的区别/](https://www.geeksforgeeks.org/difference-between-spinlock-and-semaphore/)

**1。**[**Semaphore**](https://www.geeksforgeeks.org/semaphores-in-process-synchronization/)**:**
Semaphore 基本上是一种通过使用一个简单的整数值来管理并发进程的技术，用于控制多个进程上的访问，避免操作系统中的多任务等系统中的临界区问题。这是一个非负变量，在线程间共享。它包括进程、计数器的等待列表，还支持两种不同类型的原子操作，即进程同步的等待和信号。它分为二进制和计数信号量。

*   [**二进制信号量**](https://www.geeksforgeeks.org/semaphores-in-process-synchronization/)–二进制信号量只有两个值 0 和 1。它通过多个进程来处理或移除关键部分的问题。二进制信号量也称为互斥锁。
*   **计数信号量**–这有助于控制对包含多个实例的资源的访问。这些值具有不受限制的值域。它计算可用资源的数量。

**2。**
自旋锁是一种锁定系统机制。它允许线程获取它，只需在循环中等待，直到锁可用，即线程在循环或旋转中等待，直到锁可用。自旋锁保持一小段时间。自旋锁在多处理器系统中很有用。

**自旋锁和信号量的区别:**

<figure class="table">

| **序列号**

 | **自旋锁** | **信号量** |
| 1. | 自旋锁只能用于互斥。 | 信号量可以用于互斥或计数信号量。 |
| 2. | 自旋锁是一种低级同步机制。 | 信号量是一种信号机制。 |
| 3. | 自旋锁在任何给定时间只允许一个进程访问临界区。 | 信号量允许超过一个进程在任何给定的时间访问关键部分。 |
| 4. | 如果长时间持有自旋锁，可能会造成浪费。 | 在信号量中，没有处理时间和资源的资源浪费。 |
| 5. | 一次只允许一个线程获取锁，并继续执行关键部分。 | 允许一个或几个线程访问临界区。 |
| 6.  | 自旋锁非常有效，因为它们只在短时间内被阻塞。 | 信号量保持的时间更长。为了访问它的控制结构，它使用自旋锁。 |
| 7. | 在 spinlock 中，一个等待锁的进程将通过连续轮询锁来保持处理器忙碌。 | 在信号量中，一个进程正在等待一个信号量进入睡眠状态，随时被唤醒，并再次尝试锁定。 |
| 8. | 自旋锁仅对一个进程有效。 | 信号量可用于不同进程之间的同步。 |
| 9. | 在 spinlock 中，等待锁的进程将立即获得对关键区域的访问，因为该进程将持续轮询锁。 | 在信号量中，等待锁的进程可能不会在锁一释放就进入临界区，因为进程已经进入睡眠状态，当它被唤醒时，它将进入临界区。 |
| 10. | 这是一个繁忙的等待过程。 | 这是睡眠等待过程。 |
| 11. | 自旋锁只能有两个值——锁定和解锁 | 在信号量中，互斥体的值为 1 或 0，但是如果用作计数信号量，它可以有不同的值。 |
| Twelve | 在单处理器系统中，自旋锁不是很有用，因为它们会在每次轮询锁时让处理器保持忙碌，从而禁止任何其他进程运行。 | 在单处理器系统中，信号量很方便，因为在等待锁的时候，信号量不会让处理器忙。 |
| 13. | 在自旋锁中，建议在持有自旋锁时禁用中断。 | 信号量可以在中断使能的情况下锁定。 |
| 14. | 当未能获得锁时，线程在等待锁时无法休眠，但它会继续尝试获得锁的循环。 | 当无法获得锁时，线程进入睡眠等待锁。 |

</figure>