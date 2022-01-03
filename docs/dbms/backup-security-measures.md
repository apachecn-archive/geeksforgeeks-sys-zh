# 后备安全措施

> 原文:[https://www.geeksforgeeks.org/backup-security-measures/](https://www.geeksforgeeks.org/backup-security-measures/)

**备份和恢复策略**对于大多数操作系统来说是必不可少的。许多系统管理员使用分层备份计划。书面程序和规则是系统管理的必要元素。备份文件是一项重要的系统管理员任务。每当系统出现故障时，备份文件用于将系统恢复到以前的状态。备份加密是有助于全面安全策略的众多活动之一。

**备份类型:**

1.  **完全备份–**
    完全备份是将每个文件(包括系统和用户文件)写入备份介质的备份。完全备份不会检查文件自上次备份以来是否有变化，它只是盲目地将所有内容写入备份介质。
2.  **增量备份–**
    检查文件修改时间。如果修改时间比上次备份时间晚，则进行备份，否则不进行备份。增量备份也用于完整备份。它比完全备份更快。增量备份的一个主要缺点是恢复时间较长。增量备份会带来操作员错误的威胁。

*   **差异备份–**
    它包含自上次完全备份以来修改的所有文件，使得仅使用上次完全备份和上次差异备份就可以执行完全恢复。*   **Network Backup –**
    It backing up a file system from one machine onto a backup device connected to another machine. It is referred to as a remote or network backup.

    数据是业务的命脉，在生产服务器上处于活动状态或在磁带上处于保留状态时，必须防范恶意意图。

    **后备保障**措施如下:

    *   **分配责任、职责和权限–**
        存储安全功能应包含在公司的安全政策中。一些公司创建了一个存储团队来进行备份。即使创建了单独的团队，公司仍必须将任何存储和备份安全措施与保护基础架构其余部分的措施相集成。它提供了深度防御保护。如果数据是高度敏感的，那么职责被划分给若干工作成员。
    *   **评估与信息安全相关的存储风险–**
        [风险评估](https://www.geeksforgeeks.org/risk-assessment/)是一个结构化和系统化的程序，依赖于对危害的正确识别。管理人员必须检查其备份方法的每一步，寻找
        安全漏洞。有必要对整个备份过程进行风险分析。数据在整个环境中重复出现很多次。重要的是要有策略和程序来很好地了解数据在任何时间点的位置。
    *   **制定信息保护计划–**
        多层数据保护系统用于为存储网络提供安全性。身份验证、授权、加密和审计是多层保护系统的示例。在数据存储到硬盘时对其进行加密，甚至阻止其他有权访问该系统的人访问这些文件。
    *   **围绕信息保护和安全交流流程–**
        是时候定义流程以确保敏感数据得到适当保护和处理了。重要的是确保负责执行安全的人员了解情况并接受培训。安全策略是分配责任、职责和权限的最重要方面。