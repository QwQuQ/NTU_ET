---
aliases:
  - 阵列乘法器
tags:
  - multiplier
  - digital_circuits
---
![[Array Multiplier.png]]

通过将[[Partial Products|部分积]]累加起来，我们可以得到计算的结果。阵列乘法器使用加法器阵列进行部分积的累加。上图中的HA表示[[Half Adder|半加器]]，FA表示[[Full Adder|全加器]]。
总共需要N-1个M位的加法器。

# 延时

在阵列乘法器中，不同的关键路径拥有同样的长度，延时为：
$$t_p\approx [(M-1)+(N-2)]\cdot t_{carry}+(N-1)\cdot t_{sum}+t_{and}$$上式中：
- $t_{carry}$：输入和输出进位之间的传播延时
- $t_{sum}$：全加器输入进位与$S$之间的延时
- $t_{and}$：与门的传播延时
