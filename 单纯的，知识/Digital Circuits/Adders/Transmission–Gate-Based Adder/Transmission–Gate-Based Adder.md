---
aliases:
  - 传输门型加法器
tags:
  - Adder
---
全加器可以用多路开关和XOR门设计
![[Pasted image 20241021213808.png|500]]
# 表达式
中间值：
$$P=A_i \oplus B_i$$
结果：
$$S=P\oplus C_i=\overline{\overline{P}\ \overline{C_i}+PC_i}$$
$$C_o=A_iB_i+PC_i=\overline{\overline{P}\ \overline{A_i}+P\overline{C_i}}$$
# 特点
- 和与进位输出有近似的延时