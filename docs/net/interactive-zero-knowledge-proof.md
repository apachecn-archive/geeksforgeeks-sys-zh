# 互动零知识证明

> 原文:[https://www . geesforgeks . org/interactive-零知识证明/](https://www.geeksforgeeks.org/interactive-zero-knowledge-proof/)

[零知识证明(ZKP)](https://www.geeksforgeeks.org/zero-knowledge-proof/) 的目标是“验证者”通过满足某些关系而不向其他任何人透露见证，证明自己是被称为“验证者”的某些信息的拥有者。交互式零知识证明需要验证者和证明者的实时交互。

零知识证明的基本思想最早出现在 1985 年，当时开发人员沙菲·戈德瓦瑟、查尔斯·拉科夫和希尔维奥·米卡利向世界提出了“知识复杂性”的概念，这个概念是零知识证明的前身。

**用离散算法进行交互式零知识证明:**

1.  桑奇塔想向萨钦证明她知道价值信息，这样 y = g^'Witness'等于 g。
2.  桑奇塔从一组值 z 中挑选随机值 x，计算 t = g^x，并将 t 发送给萨钦。
3.  萨钦从集合 Z 中挑选随机值 c，并将其发送给桑奇塔。
4.  Sanchita 计算 r = x-c* '证人'，并将 r 返回给 Sachin。
5.  萨钦检查 t= g^r * y^c 是否成立(因为 r= x-c* '证人'，y= g^'Witness'，通过简单的替换，g^(x-c*'Witness')* g ^ c* '证人' = g^x = t)。
6.  萨钦不知道“证人”的价值，但通过检查 t = g^r * y^c，他可以证实桑奇塔确实知道“证人”的价值。

**交互零知识证明的问题:**

*   **有限可转移性–**
    为了再次向另一个验证者证明相同的证明，需要重复整个过程。
*   **不可索赔–**
    互动 ZKP 要求验证者和证明者同时在线，这使得整个过程不可索赔。

**应用:**

*   **核裁军–**
    2016 年，普林斯顿等离子体物理实验室和普林斯顿大学展示了可能具有适用性的技术。它将允许核查人员确认一个物体是否是核武器，而无需记录、分享或披露可能是秘密的内部运作。
*   **认证系统–**
    用户无需向系统透露密码即可验证密码。零知识密码证明是一种特殊的零知识知识证明，解决了有限的密码大小，因为大多数 ZKP 协议需要更大的随机输入。

针对**交互**零知识证明面临的问题，我们进一步实现了[非交互零知识证明](https://www.geeksforgeeks.org/zero-knowledge-proof/)，使其在现实应用中具有可扩展性。