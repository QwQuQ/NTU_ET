---
aliases:
  - 超前进位加法器
tags:
  - adder
  - digital_circuits
---
超前进位加法器避免了逐级的进位传递。可以发现进位存在如下递推关系：
$$C_{o,n}=f(A_n,B_n,C_{o,n-1})=G_n+P_nC_{o,n-1}$$
递推关系展开后可以得到：
$$C_{o,n}=G_n+P_n\left(G_{n-1}+P_{n-1}\left(\cdots+P_1\left(G_0+P_0C_{i,0}\right)\right)\right)$$
其中$C_{i,0}$通常为$0$，$G$和$P$为[[Full Adder#中间信号|全加器中间信号]]

这样展开后，最终的进位输出与前面的位无关，代价是额外的逻辑门。

# 例子

4位超前进位加法器的进位产生等式为：
$$C_4=G_3+P_3G_2+P_3P_2G_1+P_3P_2P_1G_0+P_3P_2P_1P_0C_0$$
电路实现为（好复杂）：
![[Carry-Look-Ahead Adder.png]]