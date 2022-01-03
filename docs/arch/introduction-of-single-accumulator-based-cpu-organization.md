# 基于单累加器的 CPU 组织介绍

> 原文:[https://www . geesforgeks . org/基于单累加器的 cpu 组织简介/](https://www.geeksforgeeks.org/introduction-of-single-accumulator-based-cpu-organization/)

计算机出现在计算机历史的早期，有基于累加器的中央处理器。在这种类型的中央处理器组织中，累加器寄存器隐式用于处理程序的所有指令，并将结果存储到累加器中。该中央处理器组织使用的指令格式是**一个地址字段**。因此，中央处理器被称为**一地址机**。

基于单累加器的中央处理器组织的要点是:

1.  在这种中央处理器结构中，第一个算术逻辑单元操作数总是存储在累加器中，第二个操作数存在于寄存器或存储器中。
2.  累加器是默认地址，因此在数据操作之后，结果被存储到累加器中。
3.  在这种类型的组织中使用一个地址指令。

```
The format of instruction is: Opcode + Address
```

操作码指示要执行的操作类型。
在基于单累加器的 CPU 组织中，主要执行两种类型的操作:

1.  **数据传输操作–**
    在这种类型的操作中，数据从源传输到目的地。

```
For ex: LOAD X, STORE Y 
```

这里，LOAD 是存储器读操作，即数据从存储器传输到累加器，STORE 是存储器写操作，即数据从累加器传输到存储器。

*   **ALU operation –**
    In this type of operation, arithmetic operations are performed on the data.

    ```
    For ex: MULT X 
    ```

    其中 X 是操作数的地址。本例中的 MULT 指令执行操作，

    ```
    AC <-- AC * M[X] 
    ```

    交流是累加器，M[X]是位于位置 X 的存储字

    这种类型的 CPU 组织首先用于 **PDP-8 处理器**，用于过程控制和实验室应用。它已经完全被新的基于通用寄存器的中央处理器所取代。

    **优势–**

    *   其中一个操作数始终由累加器寄存器保存。这导致指令较短，内存空间较少。
    *   指令周期占用的时间更少，因为它节省了从内存中提取指令的时间。

    **缺点–**

    *   当计算复杂的表达式时，由于使用许多短指令来执行它，程序的大小会增加。因此，内存大小增加。
    *   随着程序指令数量的增加，执行时间也会增加。