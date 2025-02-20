---
aliases: 
tags:
  - digital
---

- Datapath is the core of the system
  数据通路是系统的核心
- All computations are performed in the datapath
  所有计算都在数据通路中执行
- A typical datapath consists of an [[单纯的，知识/Digital/Interconnect/Interconnect|Interconnection]] of basic combinational functions such as logic gates (NAND, XOR, etc.) and arithmetic modules ([[Adder]]s, [[Multiplier]]s, etc.)
  典型的数据通路由基本组合功能的**互连**组成，如逻辑门（NAND、XOR等）和算术模块（加法器、乘法器等）
- Results from the datapath are stored in [[Memory]]
  数据通路的结果存储在**存储器**中
- [[Control Unit]]s determines the sequence of executions in the data path
  **控制单元**决定数据通路中的执行顺序
- Intermediate results are stored in [[Memory#^78cfb0|registers]]
  中间结果存储在**寄存器**中