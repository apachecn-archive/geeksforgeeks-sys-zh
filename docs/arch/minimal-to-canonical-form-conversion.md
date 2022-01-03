# 最小到范式转换

> 原文:[https://www . geesforgeks . org/极简到规范形式转换/](https://www.geeksforgeeks.org/minimal-to-canonical-form-conversion/)

[规范形式](https://www.geeksforgeeks.org/canonical-and-standard-form/)也称为标准形式，我们直接从真值表中获得它，因此我们在每个**小项**中有所有正规或互补形式的变量。

极简形式到规范形式的转换有 3 个步骤。

*   求最小形式的变量总数。*   找出每个小项中缺少的变量。*   Try to apply operation for converting min to canonical term using one(1) or zero(o) logic.

    乘积和(SOP)形式到规范形式的转换–
    规则集与上述相同。

    **示例-1:**

    ```
    Input : 
    Y=A+B'C 
    **Output :**
    (A.B.C)+(A.B.C')+(A.B'.C)+(A.B'.C')+(A'.B'.C) 
    ```

    ****解释–****

     ***   **第一步:**
        找出以极小形式出现的变量的总数，像这样出现的变量有甲、乙、丙
    *   **Step-2:**
        找出每个项中缺少的变量，像这样在这个项中，在小项中缺少的变量(0)是 B 和 C，在小项中缺少的变量(1)是 a
    *   **Step-3:**
        尝试使用一(1)或零(o)逻辑应用将 min 转换为规范项的运算，在这种情况下，它是 SOP 形式，因此我们将一(1)与每个小项进行 AND 运算，其中变量在简单项中是不存在的，如果我们将每个小项乘以一(1)，那么对结果方程没有影响，因此在这种情况下，我们将一(1)替换为 Sum(变量+变量的补码)，然后使用切换代数的性质进一步求解。

    **转换步骤–**

    ```
    = A+B.C 
    = (A.1)+(B.C.1) 
    = (A.(B+B'))+((A+A').(B.C)) 
    = ((A.B.C)+(A.B.C')+(A.B'.C)+(A.B'.C')+(A'.B'.C))  
    ```

    总和乘积(POS)形式到规范形式的转换–
    规则集与上述相同。

    **示例-2:**

    ```
    Input :
    Y=(A+B+C).(A'+C)

    Output :
    (A+B+C').(A'+C+B).(A'+C+B') 
    ```

    **解释–**

    1.  **第一步:**
        找出以极小形式出现的变量的总数，像这样出现的变量有甲、乙、丙
    2.  **Step-2:**
        找出每个项中缺少的变量，就像这样，这个缺少的变量是 maxterm(1)中的 C
    3.  **Step-3:**
        尝试使用一(1)或零(o)逻辑应用将极小项转换为规范项的操作，在这种情况下，它是 POS 形式，因此我们将零(0)OR 到每个最大项，其中变量在简单项中不存在如果我们将每个最大项加零(0)，那么对结果方程没有影响，因此在这种情况下，在这之后，我们用乘积(变量*变量的补码)替换零(0)，然后使用切换代数的属性进一步求解。

    **转换步骤–**

    ```
    = (A+B+C).(A'+B) 
    = (A+B+C').(A'+(B.B')+C)
    = (A+B+C').(A'+C+B).(A'+C+B') 
    ```**