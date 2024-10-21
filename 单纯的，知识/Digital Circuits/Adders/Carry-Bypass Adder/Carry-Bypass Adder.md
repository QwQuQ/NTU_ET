---
aliases:
  - 进位旁路加法器
tags:
  - adder
  - digital_circuits
---
![[Carry-Bypass Adder_1.png]]

[[Full Adder#中间信号|进位传播信号]]$P$可以用来加速进位链中的进位操作。当$P$有连续的高电平时，进位输入可以通过旁路晶体管立即进入下一模块，这一操作被称为进位旁路加法器。

[[Manchester Carry Gates|曼彻斯特进位链加法器]]的进位链也可以用旁路晶体管改良。通过添加受到$BP$控制的传输管即可实现这一目的。
![[Carry-Bypass Adder_2.png]]

# 特点

- Either carry bypass or generated in the chain.
- In either case, delay is smaller
- $BP=\prod{P_n}$
# 延时

![[Carry-Bypass Adder_3.png]]

上图假设了一个$N$位的加法器，被分成了$\frac{N}{M}$个等长的旁路级，每一级含有$M$位，灰色关键路径的传播延时$t_p$可以近似表达为：
$$t_p\approx t_{setup}+M\cdot t_{carry}+\frac{N}{M-1}t_{bypass}+(M-1)t_{carry}+t_{sum}$$
上式中：
- $t_{setup}$：形成[[Full Adder#中间信号|进位产生信号]]$G$和[[Full Adder#中间信号|进位传播信号]]$P$所需要的固定时间
- $t_{carry}$：通过1位的传播延时。最坏情况下通过具有$M$位的进位链的传播延时大约为$M\cdot t_{carry}$
- $t_{bypass}$：通过一级旁路多路开关的传播延时
- $t_{sum}$：最后一级产生$S$所需要的时间

