# 最高储物柜协议(HLP)

> 原文:[https://www.geeksforgeeks.org/highest-locker-protocol-hlp/](https://www.geeksforgeeks.org/highest-locker-protocol-hlp/)

**最高锁协议(HLP)** 是一种关键的资源共享协议，是优先级继承协议的扩展，引入该协议是为了克服优先级继承协议的局限性。在这个关键资源共享协议中，每个关键资源都被分配一个最高优先级值。该值是所有可能请求保留此关键资源的任务的最大优先级。

**HLP 的基本概念:**
最高储物柜协议的基本概念是基于上限优先级值。当任务持有关键资源时，其优先级会更改为关键资源的最高优先级值。如果一项任务拥有多个关键资源，则所有最高优先级值中的最大值将被指定为该任务的优先级。

**HLP 工作时间:**

*   每个任务所需的资源都是在编译前找到的。
*   最初，最高优先级值被分配给每个关键资源。
*   关键资源的最高优先级值计算为所有可能请求保留该关键资源的任务的最大优先级。
*   当任务拥有关键资源时，相应的最高优先级值将被指定为该任务的优先级。
*   获取多个关键资源的任务被分配最高优先级值。
*   此外，根据分配的优先级执行。

**HLP 特色:**

*   当 HLP 用于资源共享时，一旦任务拥有所需的关键资源，它就不会被进一步阻止。
*   在任务可以容纳一个资源之前，该任务可能需要的所有资源都应该是空闲的。
*   它防止任务陷入死锁或链阻塞。

**HLP 的优势:**
以下是最高储物柜协议的优势:

*   它有助于几项任务共享关键资源。
*   它避免了任务间无边界的优先级反转。
*   它克服了优先级继承协议的局限性。
*   它可以防止死锁，因为任务只有一个资源，该任务所需的所有其他资源都必须是空闲的。
*   使用最高锁协议，任务不能进入链阻塞。

**HLP 的劣势:**
最高锁协议的主要劣势是**继承相关优先级反转**。

继承相关优先级反转发生在获取关键资源的低优先级任务的优先级值使用上限规则被分配最高优先级时，则不需要该资源的中间优先级任务不能执行并经历继承相关优先级转换。