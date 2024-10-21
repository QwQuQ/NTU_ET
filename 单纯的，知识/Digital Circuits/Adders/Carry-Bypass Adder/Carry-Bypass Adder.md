---
aliases:
  - 进位旁路加法器
tags:
  - TODO
  - adder
---
![[Carry-Bypass Adder.png]]

[[Full Adder|全加器]]中的进位传播信号$P$可以用来加速进位链中的进位操作。当$P$有连续的高电平时，进位输入可以通过旁路晶体管立即进入下一模块，这一操作被称为进位旁路加法器。

# 特点

- Either carry bypass or generated in the chain.
- In either case, delay is smaller
- $BP=$