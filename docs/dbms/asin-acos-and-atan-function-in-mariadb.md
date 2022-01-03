# 马里亚数据库中的 ASIN()，ACOS()和 ATAN()函数

> 原文:[https://www . geesforgeks . org/asin-acos-and-atan-function-in-Maria db/](https://www.geeksforgeeks.org/asin-acos-and-atan-function-in-mariadb/)

**1。ASIN 函数:**
在马里亚数据库中，ASIN 函数用于求一个数的反正弦。在该函数中，一个数字将作为参数传递，并且该函数将返回该数字的反正弦。只有当数字在-1 到 1 的范围内时，函数才会返回有效输出，否则，它将返回空值作为输出。

**语法:**

```
ASIN(number)
```

**参数:**必选。数值。
**数字:**用来计算反正弦的数字。数字的范围必须在-1 到 1 之间。

**示例-1 :**

```
SELECT ASIN(1);
```

**输出:**

```
1.5707963267948966
```

**示例-2 :**

```
SELECT ASIN(2.3);
```

**输出:**

```
NULL
```

**示例-3 :**

```
SELECT ASIN(0.41);
```

**输出:**

```
0.42245406218675574
```

**2。ACOS 函数:**
在马里亚数据库中，ACOS 函数用于求一个数的弧余弦。在这个函数中，一个数字将作为参数传递，这个函数将返回这个数字的反余弦值。只有当数字在-1 到 1 的范围内时，函数才会返回有效输出，否则，它将返回空值作为输出。

**语法:**

```
ACOS(number)
```

**参数:**必选。数值。
**数字:**用来计算弧余弦的数字。数字的范围必须在-1 到 1 之间。

**示例-1 :**

```
SELECT ACOS(-0.6);
```

**输出:**

```
2.214297435588181
```

**示例-2 :**

```
SELECT ACOS(1);
```

**输出:**

```
0
```

**示例-3 :**

```
SELECT ACOS(1.9);
```

**输出:**

```
NULL
```

**3。ATAN 函数:**
在 MariaDB 中，ATAN 函数用于求一个数的反正切或者 n 和 m 的反正切，在这个函数中，一个数将作为参数传递或者 n 和 m 将作为第二类语法传递。这个函数将返回该数的反正切。当使用第二种语法时，m，n 的符号用于决定结果的象限。

**语法-1 :**

```
ATAN(number)
```

**参数:**必选。数值。
**数字:**用于计算反正切的数字。

**语法-2 :**

```
ATAN(n, m)
```

**参数:**必选。两个数值。
**n，m :** 用于计算反正切的两个值。

**示例-1 :**

```
SELECT ATAN(-1.4);
```

**输出:**

```
-0.9505468408120751
```

**示例-2 :**

```
SELECT ATAN(1, 3);
```

**输出:**

```
0.3217505543966422
```

**示例-3 :**

```
SELECT ATAN(0.6);
```

**输出:**

```
0.5404195002705842
```