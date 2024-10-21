---
aliases:
  - 平方根进位选择加法器
tags:
  - adder
  - digital_circuits
---
考虑，[[Carry-Select Adder|进位选择加法器]]中于后面几级多路开关的输入，会发现进位的输入远早于多路开关控制信号的输入。所以适当延长进位的传播延时可以达到更优解。

![[Square-Root Carry-Select Adder.png]]

# 特点

- 最开始的级位数最少
- 每一级增加1位，所以级数约为$\sqrt{2N}$

# 延时

$$t_p=t_{setup}+M\cdot t_{carry}+\sqrt{2N}\cdot t_{mux}+t_{sum}$$

